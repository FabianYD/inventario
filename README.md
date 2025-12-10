# Sistema de Inventario

Este proyecto es un sistema de inventario construido con [Laravel](https://laravel.com), utilizando [Filament](https://filamentphp.com) para el panel administrativo y configurado con soporte para API (Laravel Sanctum).

## Requisitos

- PHP ^8.2
- PostgreSQL
- Node.js & NPM
- Composer

## Instalación

Sigue estos pasos para configurar el proyecto en tu entorno local:

1.  **Clonar el repositorio**

    ```bash
    git clone <url-del-repositorio>
    cd inventario
    ```

2.  **Instalar dependencias de PHP**

    ```bash
    composer install
    ```

3.  **Instalar dependencias de JavaScript**

    ```bash
    npm install
    npm run build
    ```

4.  **Configuración del Entorno**

    Copia el archivo de ejemplo de configuración:

    ```bash
    cp .env.example .env
    ```

    Abre el archivo `.env` y configura las credenciales de tu base de datos **PostgreSQL**:

    ```env
    DB_CONNECTION=pgsql
    DB_HOST=127.0.0.1
    DB_PORT=5432
    DB_DATABASE=inventario
    DB_USERNAME=tu_usuario
    DB_PASSWORD=tu_contraseña
    ```

5.  **Generar Key de la Aplicación**

    ```bash
    php artisan key:generate
    ```

6.  **Ejecutar Migraciones**

    Una vez configurada la base de datos, ejecuta las migraciones:

    ```bash
    php artisan migrate
    ```

7.  **Crear Usuario Administrador (Filament)**

    Para acceder al panel administrativo, necesitas crear un usuario:

    ```bash
    php artisan make:filament-user
    ```

    Sigue las instrucciones en la terminal para ingresar nombre, correo y contraseña.

## Ejecución

Para iniciar el servidor de desarrollo:

```bash
php artisan serve
```

El panel administrativo estará disponible en `/admin` (por defecto, o la ruta que hayas configurado).
La API está configurada y lista para usarse.

## Tecnologías

- **Framework:** Laravel 11/12
- **Admin Panel:** Filament
- **Base de Datos:** PostgreSQL
- **API:** Laravel Sanctum

## Contribución

1.  Haz un Fork del proyecto
2.  Crea tu rama de funcionalidad (`git checkout -b feature/AmazingFeature`)
3.  Haz Commit de tus cambios (`git commit -m 'Add some AmazingFeature'`)
4.  Push a la rama (`git push origin feature/AmazingFeature`)
5.  Abre un Pull Request
