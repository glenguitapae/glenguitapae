## Contenidoss

| File/folder           | Description                                |
|-----------------------|--------------------------------------------|
| `App/authPopup.js`    | Main authentication logic resides here (using popup flow). |
| `App/authRedirect.js` | Use this instead of `authPopup.js` for authentication with redirect flow. |
| `App/authConfig.js`   | Contains configuration parameters for the sample. |
| `App/apiConfig.js`    | Contains web API scopes and coordinates. |
| `App/policies.js`     | Contains B2C custom policies and user-flows.  |

## Prerequisitos

- [Node.js]
- Browser.
- Azure AD B2C tenant..
- Cuenta en el Azure AD B2C tenant.

## Setup

### Instalación

```console
    cd identity-b2c-js-spa
    npm install
```

#### Configure la aplicación (JavaScript SPA) para usar el registro de su aplicación

Abra el proyecto en su IDE (como Visual Studio Code) para configurar el código.

> En los pasos a continuación, "ClientID" es lo mismo que "Application ID" o "AppId".

Abra el archivo `App\authConfig.js`. Después:

1. Busque la clave `clientId` y reemplace el valor existente con el ID de la aplicación (clientId) de la aplicación `identity-b2c-js-spa` copiada de Azure Portal.
1. Busque la clave `redirectUri` y reemplace el valor existente con la dirección base del proyecto Identity-b2c-js-spa (por defecto, `http://localhost:6420`).

Abra el archivo `App\policies.js`. Después:

1. Busque la clave `policies.names` y reemplácela con los nombres (ID) de sus políticas/flujos de usuario, p. `b2c_1_susi_reset_v2`.
1. Busque la clave `policies.authorities` y reemplácela con las cadenas de autoridad de sus políticas/flujos de usuario
1. Busque la clave `policies.authorityDomain` y reemplácela con el dominio de su autoridad

Abra el archivo `App\apiConfig.js`. Después:

1. Busque la clave `b2cScopes` y reemplace el valor existente con el alcance de su API web
1. Busque la clave `webAPI` y reemplace el valor existente con las coordenadas de su API web

## Ejecutando la muestra

```consola
    cd identidad-b2c-js-spa
    inicio de npm
```

## Explorar la muestra

1. Abra su navegador y vaya a `http://localhost:6420`.
1. Haga clic en el botón **SIGN IN** en la esquina superior derecha.
