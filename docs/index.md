<table id="myTable">
  <thead>
    <tr>
      <th>Datum</th>
      <th>Aktion</th>
      <th>Kategorie</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>2025-03-01</td><td>Beispielaktion A</td><td>Skandal</td></tr>
    <tr><td>2025-04-15</td><td>Gesetzesinitiative B</td><td>Gesetzgebung</td></tr>
  </tbody>
</table>

<input type="text" id="searchInput" placeholder="Filter nach Kategorie...">

<script>
  const input = document.getElementById('searchInput');
  input.addEventListener('keyup', function() {
    const filter = input.value.toLowerCase();
    const rows = document.querySelectorAll('#myTable tbody tr');
    rows.forEach(row => {
      const category = row.cells[2].textContent.toLowerCase();
      row.style.display = category.includes(filter) ? '' : 'none';
    });
  });
</script>
