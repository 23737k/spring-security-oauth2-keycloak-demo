# Configuración de OAuth2 para Keycloak con Spring Boot

## Configuración Previa de Keycloak

1. **Ejecutar Keycloak**:
    - Si se descargó localmente, ve a la carpeta `bin`.
    - Abre una terminal bash (por ejemplo, `Git Bash Here`) y ejecuta:
      ```bash
      ./kc.sh start-dev --http-port=8180
      ```
2. **Registrar un Usuario Admin**:
    - Ve a `http://localhost:8180` y registra un usuario administrador.
    - Luego, inicia sesión con este usuario.
3. **Crear un Nuevo Realm**:
    - Dentro del realm creado, crea un nuevo cliente:
        - Especifica el `client_id`.
        - Selecciona la opción **Client authentication**.
        - Deselecciona **Direct access grants**.
        - Especifica el `redirect_uri`:
          ```http://localhost:<port>/login/oauth2/code/<client_id>```
4. **Crear Usuarios**:
    - Basta con especificar el `username`.
    - Luego de guardar, especifica las credenciales (pueden ser temporales o no).




