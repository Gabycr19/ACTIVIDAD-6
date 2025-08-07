# ACTIVIDAD-6
:root {
  --primary: rgb(177, 6, 6);
  --secondary: #94ce0c;
  --success: oklab(32.681% 0.09236 -0.11722);
  --danger: #043d22;
  --warning: #2e2c12;
  --font: 'Segoe UI', sans-serif;
  --shadow: 0 4px 8px rgba(19, 52, 54, 0.1);
  --radius: 0.5rem;
  --transition: 0.3s ease;
}

body {
  font-family: var(--font);
  margin: 0;
  padding: 0;
  background: #d18989;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  padding: 2rem;
}

/* Navbar */
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 1rem;
  background: var(--primary);
  color: rgb(216, 226, 231);
}
.navbar__menu {
  list-style: none;
  display: flex;
  gap: 1rem;
}
.navbar__menu li a {
  color: rgb(231, 176, 24);
  text-decoration: none;
}

/* Botones */
.btn {
  padding: 0.5rem 1rem;
  border: none;
  border-radius: var(--radius);
  cursor: pointer;
  transition: var(--transition);
  background: #080d13;
  color: #1f968c;
}
.btn:hover {
  opacity: 0.9;
}
.btn--primary { background: var(--primary); }
.btn--secondary { background: var(--secondary); }
.btn:disabled { background: #e1dde971; cursor: not-allowed; }

/* Tarjetas */
.card {
  background: rgb(221, 220, 160);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  padding: 1rem;
  margin: 1rem 0;
}

/* Formulario */
.form input, .form select {
  display: block;
  width: 100%;
  padding: 0.5rem;
  margin-bottom: 1rem;
  border-radius: var(--radius);
  border: 1px solid #0f110e;
}

/* Modal */
.modal {
  position: fixed;
  top: 0; left: 0;
  width: 100vw; height: 100vh;
  background: rgba(17, 17, 19, 0.5);
  display: none;
  align-items: center;
  justify-content: center;
}
.modal__content {
  background: rgb(22, 5, 17);
  padding: 2rem;
  border-radius: var(--radius);
  position: relative;
}
.modal__close {
  position: absolute;
  top: 0.5rem;
  right: 1rem;
  cursor: pointer;
  font-size: 1.5rem;
}

/* Tooltip */
.tooltip {
  position: relative;
}
.tooltip::after {
  content: attr(data-tooltip);
  position: absolute;
  background: #333;
  color: #000000;
  padding: 0.4rem;
  border-radius: var(--radius);
  top: -2.5rem;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0;
  pointer-events: none;
  transition: var(--transition);
}
.tooltip:hover::after {
  opacity: 1;
}

/* Alertas */
.alert {
  padding: 1rem;
  border-radius: var(--radius);
  margin-bottom: 1rem;
  color: rgb(15, 15, 5);
}
.alert--success { background: var(--success); }
.alert--danger { background: var(--danger); }
.alert--warning { background: var(--warning); }

/* Badge */
.badge {
  background: var(--danger);
  color: rgb(107, 145, 109);
  padding: 0.2rem 0.5rem;
  border-radius: 999px;
  font-size: 0.8rem;
  margin-left: 0.5rem;
}

/* Tabs */
.tabs {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
}
.tab {
  background: #e6ebe6;
  padding: 0.5rem 1rem;
  cursor: pointer;
  border-radius: var(--radius);
}
.tab.active {
  background: var(--primary);
  color: rgba(9, 122, 24, 0.575);
}

/* Responsive */
@media (max-width: 600px) {
  .navbar__menu {
    flex-direction: column;
    gap: 0.5rem;
  }
}
