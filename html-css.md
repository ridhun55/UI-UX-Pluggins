Button class
```css
.btn {
  display: inline-block;
  font-weight: 400;
  line-height: 1.5;
  color: #212529;
  text-align: center;
  text-decoration: none;
  vertical-align: middle;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  user-select: none;
  background-color: transparent;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  border-radius: 0.25rem;
  transition: color 0.15s ease-in-out, 
              background-color 0.15s ease-in-out, 
              border-color 0.15s ease-in-out, 
              box-shadow 0.15s ease-in-out;
}
.btn:hover {
  color: #212529;
}
.btn:focus {
  outline: 0;
  box-shadow: 0 0 0 0.25rem rgba(13, 110, 253, 0.25);
}
.btn:disabled, .btn.disabled{
  pointer-events: none;
  opacity: 0.65;
}
.btn:active, .btn.active, .btn .active{
  background:red;
}
```

button primary

```css
.btn-primary {
  color: #fff;
  background-color: #0d6efd;
  border-color: #0d6efd;
}
.btn-primary:hover {
  color: #fff;
  background-color: #0b5ed7;
  border-color: #0a58ca;
}
.btn-primary:focus {
  color: #fff;
  background-color: #0b5ed7;
  border-color: #0a58ca;
  box-shadow: 0 0 0 0.25rem rgba(49, 132, 253, 0.5);
}
.btn:active, .btn.active, .btn .active{
  color: #fff;
  background-color: #0a58ca;
  border-color: #0a53be;
}

```
box shadow inset
```css
box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.12),
            inset 0 1px 2px rgba(0, 0, 0, 0.24);
```
