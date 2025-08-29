# no-coming-videos-on-youtube
Hide all "coming" videos on youtube feed - suscriptions page.


English:
1. Install [**Stylus**](https://addons.mozilla.org/es/firefox/addon/styl-us/) on your browser.
2. Create a new style for `youtube.com`.
3. Use this CSS:

```css
/* Hide "upcoming" in the suscription feed of YouTube */
ytd-thumbnail-overlay-time-status-renderer[overlay-style="UPCOMING"] {
  display: none !important;
}

/* Alternative: show a black box instead of not showing them at all */
ytd-thumbnail-overlay-time-status-renderer[overlay-style="UPCOMING"]::before {
  content: "";
  position: absolute;
  inset: 0;
  background: black;
  z-index: 10;
}
```

* The first rule erase the videos from the feed.
* The second rule -if activated- puts a black box instead.

Escodner todos los videos "coming" de la vista de suscripciones.
Español:
1. Instalar la extensión [**Stylus**](https://addons.mozilla.org/es/firefox/addon/styl-us/) en tu explorador de internetes favorito.
2. Creá un nuevo estilo para `youtube.com`.
3. Pegá este CSS:

```css
/* Ocultar videos "upcoming" en el feed de YouTube */
ytd-thumbnail-overlay-time-status-renderer[overlay-style="UPCOMING"] {
  display: none !important;
}

/* Alternativa: mostrar un recuadro negro en vez de borrarlos */
ytd-thumbnail-overlay-time-status-renderer[overlay-style="UPCOMING"]::before {
  content: "";
  position: absolute;
  inset: 0;
  background: black;
  z-index: 10;
}
```

* La primera regla **los elimina** del feed.
* La segunda regla (si querés activarla) hace que el recuadro quede negro en la miniatura.
