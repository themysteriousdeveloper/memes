<script>
  document.addEventListener('DOMContentLoaded', function() {
    var elems = document.querySelectorAll('.fixed-action-btn');
    var instances = M.FloatingActionButton.init(elems, options);
  });
</script>

<div class="fixed-action-btn tooltipped" data-position="top" data-tooltip="Source Code">
  <a href="https://github.com/TheMysteriousDeveloperOrg/memes" class="btn-floating btn-large red tooltipped" data-position="top" data-tooltip="Source Code">
    <i class="large material-icons tooltipped" data-position="top" data-tooltip="Source Code">tab</i>
  </a>
  <ul>
    <li><a class="btn-floating red"><i class="material-icons">insert_chart</i></a></li>
    <li><a class="btn-floating yellow darken-1"><i class="material-icons">format_quote</i></a></li>
    <li><a class="btn-floating green"><i class="material-icons">publish</i></a></li>
    <li><a class="btn-floating blue"><i class="material-icons">attach_file</i></a></li>
  </ul>
</div>
