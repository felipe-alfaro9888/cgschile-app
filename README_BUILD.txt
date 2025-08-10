Generador Grilla CGSChile — App de Escritorio (Electron + electron-builder)
==========================================================================

REQUISITOS
- Node.js 18+ y npm
- (Opcional) Apple Developer ID para firmar en macOS

PASOS RÁPIDOS
1) Instalar dependencias:
   npm install

2) Ejecutar en modo desarrollo:
   npm start

3) Generar instaladores:
   Windows: npm run dist:win
   macOS:   npm run dist:mac
   Linux:   npm run dist:linux
   (o todo a la vez): npm run dist

SALIDA
- Los instaladores quedarán en la carpeta "dist/":
  • Windows:  Generador_Grilla_CGSCHILE_win_1.0.0.exe (NSIS)
  • macOS:    Generador_Grilla_CGSCHILE_mac_1.0.0.dmg
  • Linux:    Generador_Grilla_CGSCHILE_linux_1.0.0.AppImage

NOTAS
- La app funciona 100% offline, cargando el HTML empaquetado en app.asar.
- El bloqueo por nombre del HTML se mantiene dentro del paquete, pero ya no afecta la app (la app carga su copia interna).
- Reemplaza los iconos en /build/ con tus archivos reales (PNG/ICNS/ICO).
- Si necesitas políticas más estrictas (firma de código, notarización), contáctame y te dejo los pasos.


CI en GitHub Actions
--------------------
También puedes construir los instaladores sin instalar nada en tu PC:

1) Crea un repositorio en GitHub (puede ser privado).
2) Sube TODO el contenido de este proyecto (incluida la carpeta .github/workflows/).
3) Ve a la pestaña "Actions" en GitHub y habilita los workflows si te lo pide.
4) Opcional: crea una rama "main" o "master".
5) Lanza el flujo manualmente (botón "Run workflow") o haz un push a main.
6) Cuando termine, entra a la ejecución y descarga el artefacto:
   - Windows:  Generador_Grilla_CGSCHILE_Windows_Installer (.exe)
   - macOS:    Generador_Grilla_CGSCHILE_macOS_DMG (.dmg)
   - Linux:    Generador_Grilla_CGSCHILE_Linux_AppImage (.AppImage)

Notas:
- El instalador de macOS vendrá SIN firma. Para distribuir fuera de tu equipo, conviene firmar/notarizar.
- Windows puede mostrar SmartScreen: elige "Más información" > "Ejecutar de todas formas".
