# Scroll-Responsive-Nav

Scroll Responsive Nav is a simple, light-weight javascript plugin for creating navigation bars responsive to user scroll input. 
This mini-plugin is meant to be used as a dynamic means of toggling CSS animations/classes based off of user specified thresholds.

##Usage

###Basic Call:
```
$("#main-nav").peekaboo();
```
###HTML Example:
```
<nav id="main-nav" class="navbar navbar-default navbar-fixed-top navbar-custom">
  <div class="nav-links pull-right">
    <ul class="nav navbar-nav">
      <li> <a href="#">Home</a> </li>
      <li> <a href="#">About</a> </li>
      <li> <a href="#">Contact</a> </li>
    </ul>
  </div>
</nav>
```

###CSS Required
```
.main-nav {
    background: rgba(0,0,0,0);
    text-transform: uppercase;
    border: none;
    padding: 5px;
    box-shadow: none;
}

.fade-background {
    background-color: #333332;
}

.slide-up {
    top: -60px;
}
```
##Options
<table>
<thead>
  <tr>
    <td>Options</td>
    <td>Description</td>
  </tr>
</thead>
<tbody>
  <tr>
    <td>scroll_threshold</td>
    <td>Pixel offset from window top before beginning scroll detection</td>
  </tr>
  <tr>
    <td>opaque_threshold_down</td>
    <td>Pixel offset from window top before fade-background class is applied</td>
  </tr>
  <tr>
    <td>opaque_threshold_up</td>
    <td>Pixel offset from window top before fade-background class is removed</td>
  </tr>
  <tr>
    <td>animation</td>
    <td>Toggles CSS transitions</td>
  </tr>
  <tr>
    <td>hide_class</td>
    <td>Name of CSS class to apply when scroll threshold is broken (default: scroll-up)</td>
  </tr>
  <tr>
    <td>fade_class</td>
    <td>Name of CSS class to apply when opaque threshold is broken (default: fade-background)</td>
  </tr>
  <tr>
    <td>hide_height_auto</td>
    <td>Set to false if applying custom `hide_class`, otherwise element is dynamically hidden based on element height</td>
  </tr>
</tbody>
</table>

### Full Example (Defaults):
```
$("#main-nav").peekaboo({
offset_top: $(window).height()
, scroll_threshold: ($(window).height() / 8)
, opaque_threshold_down: ($(window).height() / 4)
, opaque_threshold_up: ($(window).height() / 8)
, animation: true
, hide_class: "slide-up"
, fade_class: "fade-background"
, hide_height_auto: true
});
```

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## About the Author // WTFPL Licensing
Hey, I'm <a href="http://www.sawal.ca">Victor Sawal</a>! 
This library was created as a convenience for me, and I hope it does the same for you.
