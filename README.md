# GameVault

GameVault es una aplicación de demostración hecha con Flutter para organizar y visualizar una pequeña colección de videojuegos. Esta versión contiene una UI con pestañas (Juegos, Favoritos, Categorías), un formulario para añadir juegos y una pantalla de Ajustes.

## Descripción breve

Una app educativa para practicar widgets de Flutter y el uso de `SharedPreferences` para guardar ajustes locales.

## Requisitos

- Flutter instalado y configurado. Verifica con:

```bash
flutter --version
```

- Un emulador o dispositivo conectado (Android, iOS, Web o Desktop)

## Instalación y ejecución

1. Clona o descarga el repositorio y muévete a la carpeta del proyecto:

```bash
git clone https://github.com/ssannad862/gamevault
cd gamevaultN
```

2. Recupera las dependencias:

```bash
flutter pub get
```

3. Ejecuta la app:

```bash
flutter run
```

Para ejecutar en web (ej. Chrome):

```bash
flutter run -d chrome
```

---

## ¿Qué ajustes se guardan?

La app utiliza `SharedPreferences` a través de `lib/services/settings_service.dart`. Actualmente se guardan los siguientes ajustes:

- `darkMode` (bool): Tema oscuro; valor por defecto: `false`.
- `username` (String): Nombre de usuario; valor por defecto: `''` (cadena vacía).
- `preferredPlatform` (String): Plataforma preferida (ej. `PC`, `PS5`, `Switch`); valor por defecto: `PC`.

Cómo probarlo:

1. Abre el Drawer y entra en Ajustes.
2. Activa/desactiva el Tema oscuro, cambia el nombre y selecciona una plataforma.
3. Cierra y vuelve a abrir la app; los ajustes se conservan automáticamente.

Los métodos relevantes para persistir estos ajustes son `SettingsService.setDarkMode`, `SettingsService.setUsername` y `SettingsService.setPreferredPlatform`.
