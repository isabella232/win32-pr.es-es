---
title: Control de la autenticación
description: Algunos servidores proxy y requieren autenticación antes de conceder acceso a los recursos en Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1797f34eb4f25f8d5e345b6790489acd5fad7e2bc21e6457642a1b4ffa022f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113834"
---
# <a name="handling-authentication"></a>Control de la autenticación

Algunos servidores proxy y requieren autenticación antes de conceder acceso a los recursos en Internet. Las funciones de WinINet admiten la autenticación de servidor y proxy para sesiones HTTP. La autenticación de servidores FTP debe controlarse mediante la [**función InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Actualmente, no se admite la autenticación de puerta de enlace FTP.

## <a name="about-http-authentication"></a>Acerca de la autenticación HTTP

Si se requiere autenticación, la aplicación cliente recibe un código de estado 401, si el servidor requiere autenticación, o 407, si el proxy requiere autenticación. Con el código de estado, el proxy o servidor envía uno o varios encabezados de respuesta de autenticación: Proxy-Authenticate (para la autenticación de proxy) o WWW-Authenticate (para la autenticación del servidor).

Cada encabezado de respuesta de autenticación contiene un esquema de autenticación disponible y un dominio kerberos. Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de respuesta de autenticación. El valor de dominio kerberos distingue mayúsculas de minúsculas y define un espacio de protección en el proxy o servidor. Por ejemplo, el encabezado "WWW-Authenticate: Basic Realm="example"" sería un ejemplo de un encabezado devuelto cuando se requiere la autenticación del servidor.

La aplicación cliente que envió la solicitud puede autenticarse mediante la inclusión de un campo de encabezado de autorización con la solicitud. El encabezado Authorization contendrá el esquema de autenticación y la respuesta adecuada requerida por ese esquema. Por ejemplo, el encabezado "Authorization: Basic" se agregaría a la solicitud y se volvería a enviar al servidor si el cliente recibió el encabezado de respuesta de autenticación \<username:password> "WWW-Authenticate: Basic Realm="example"".

Hay dos tipos generales de esquemas de autenticación:

-   Esquema de autenticación básico, donde el nombre de usuario y la contraseña se envían en texto no cifrado al servidor.
-   Esquemas de desafío-respuesta, que permiten un formato de desafío-respuesta.

El esquema de autenticación básico se basa en el modelo en el que un cliente debe autenticarse con un nombre de usuario y una contraseña para cada dominio. El servidor proporciona servicios a la solicitud si se reenvia con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.

Los esquemas de desafío-respuesta permiten una autenticación más segura. Si una solicitud requiere autenticación mediante un esquema de desafío-respuesta, el código de estado adecuado y los encabezados Authenticate se devuelven al cliente. A continuación, el cliente debe volver a enviar la solicitud con una negociación. El servidor devolvería un código de estado adecuado con un desafío y, a continuación, el cliente requeriría volver a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado.

En la tabla siguiente se enumeran los esquemas de autenticación, el tipo de autenticación, el archivo DLL que los admite y una descripción del esquema.



| Scheme                                    | Tipo               | Archivo DLL                  | Descripción                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto no cifrado)                         | basic              | Wininet.dll          | Usa una cadena codificada en Base64 que contiene el nombre de usuario y la contraseña.                                                                                                                                                                                                                                                                             |
| Digest                                    | desafío-respuesta | Digest.dll           | Un esquema de desafío-respuesta que se enfrenta al uso de un valor nonce (una cadena de datos especificada por el servidor). Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor nonce especificado, el método HTTP y el identificador uniforme de recursos (URI) solicitado. La compatibilidad con la autenticación implícita se introdujo en Microsoft Internet Explorer 5. |
| NT LAN Manager (NTLM)                     | desafío-respuesta | Winsspi.dll          | Un esquema de desafío-respuesta que basa el desafío en el nombre de usuario.                                                                                                                                                                                                                                                                             |
| Microsoft Network (MSN)                   | desafío-respuesta | Msnsspc.dll          | The Microsoft Network esquema de autenticación de .                                                                                                                                                                                                                                                                                                     |
| Autenticación con contraseña distribuida (DPA) | desafío-respuesta | Msapsspc.dll         | Similar a la autenticación MSN y también se usa en Microsoft Network.                                                                                                                                                                                                                                                                           |
| Autenticación remota de frase de contraseña (RPA)    | Compuserve         | Rpawinet.dll, da.dll | Esquema de autenticación de CompuServe. Para obtener más información, vea Especificaciones [del mecanismo de RPA.](https://www.compuserve.com/)                                                                                                                                                                                                    |



 

Para cualquier cosa que no sea la autenticación básica, las claves del Registro deben configurarse además de instalar el archivo DLL adecuado.

Si se requiere autenticación, se debe usar la marca [ \_ KEEP \_ \_ CONNECTION](api-flags.md) de INTERNET FLAG en la llamada a [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) La marca KEEP CONNECTION de INTERNET FLAG es necesaria para NTLM y otros tipos de autenticación con el fin de mantener la conexión mientras se \_ completa el proceso de \_ \_ autenticación. Si no se mantiene la conexión, el proceso de autenticación debe reiniciarse con el proxy o el servidor.

Las [**funciones InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completan correctamente incluso cuando se requiere autenticación. La diferencia es que los datos devueltos en los archivos de encabezado e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) recibirían una página HTML que informa al usuario del código de estado.

### <a name="registering-authentication-keys"></a>Registro de claves de autenticación

INTERNET OPEN TYPE PRECONFIG examina los valores del Registro \_ \_ \_ **ProxyEnable**, **ProxyServer** y **ProxyOverride.** Estos valores se encuentran en **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Configuración**.

Para los esquemas de autenticación distintos de Básico, se debe agregar una clave al Registro en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Un **valor DWORD,** **Flags**, debe establecerse con el valor adecuado. En la lista siguiente se muestran los valores posibles para **el valor Flags.**

-   LA \_ AUTENTICACIÓN \_ DEL COMPLEMENTO MARCA UN CONTEXTO ÚNICO POR \_ \_ \_ \_ TCPIP (value=0x01)

    Cada socket de Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) contiene un contexto diferente. De lo contrario, se pasa un nuevo contexto para cada plantilla de dirección URL de dominio o bloque.

-   LAS \_ MARCAS DE \_ AUTENTICACIÓN DEL COMPLEMENTO PUEDEN CONTROLAR \_ LA INTERFAZ DE USUARIO \_ \_ (value=0x02)

    Este archivo DLL puede controlar su propia entrada de usuario.

-   LAS \_ MARCAS DE \_ AUTENTICACIÓN DEL COMPLEMENTO PUEDEN CONTROLAR \_ NO \_ \_ \_ PASSWD (value=0x04)

    Este archivo DLL podría ser capaz de realizar una autenticación sin solicitar al usuario una contraseña.

-   PLUGIN \_ AUTH \_ FLAGS \_ NO REALM \_ (value=0x08)

    Este archivo DLL no usa una cadena de dominio kerberos HTTP estándar. Los datos que parecen ser un dominio kerberos son datos específicos del esquema.

-   MARCAS \_ DE AUTENTICACIÓN \_ DEL COMPLEMENTO KEEP ALIVE NOT REQUIRED \_ \_ \_ \_ (value=0x10)

    Este archivo DLL no requiere una conexión persistente para su secuencia de desafío-respuesta.

Por ejemplo, para agregar la autenticación NTLM, la clave NTLM debe agregarse a **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. En **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security NTLM , se debe agregar el valor de \\  \\  \\  \\  \\  **cadena, DLLFile** y un **valor DWORD,** **Flags**. **DLLFile** debe establecerse en Winsspi.dll y **Flags** debe establecerse en 0x08.

### <a name="server-authentication"></a>Autenticación de servidor

Cuando un servidor recibe una solicitud que requiere autenticación, el servidor devuelve un mensaje de código de estado 401. En ese mensaje, el servidor debe incluir uno o varios encabezados WWW-Authenticate respuesta. Estos encabezados incluyen los métodos de autenticación que el servidor tiene disponibles. WinINet elige el primer método que reconoce.

La autenticación básica proporciona seguridad débil a menos que el canal se vincule primero con SSL o PCT.

La [**función InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada para obtener los datos.

Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer los valores [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION \_ \_ USERNAME](option-flags.md) y, a continuación, volver a enviar la solicitud al servidor.

### <a name="proxy-authentication"></a>Autenticación de proxy

Cuando un cliente intenta usar un proxy que requiere autenticación, el proxy devuelve un mensaje de código de estado 407 al cliente. En ese mensaje, el proxy debe incluir uno o varios encabezados Proxy-Authenticate respuesta. Estos encabezados incluyen los métodos de autenticación disponibles desde el proxy. WinINet elige el primer método que reconoce.

La [**función InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada.

Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer los valores [INTERNET OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) y, a continuación, volver a enviar la solicitud al proxy.

Si no se establece ningún nombre de usuario y contraseña de proxy, WinINet intenta usar el nombre de usuario y la contraseña para el servidor. Este comportamiento permite a los clientes implementar la misma interfaz de usuario personalizada que se usa para controlar la autenticación del servidor.

## <a name="handling-http-authentication"></a>Control de la autenticación HTTP

La autenticación HTTP se puede controlar con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o una función personalizada que usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o agrega sus propios encabezados de autenticación. [**InternetErrorDlg puede examinar**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) los encabezados asociados a un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para buscar errores ocultos, como códigos de estado de un servidor o proxy. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) se puede usar para establecer el nombre de usuario y la contraseña para el proxy y el servidor. Para la autenticación de MSN y DPA, se debe usar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) para establecer el nombre de usuario y la contraseña.

Para cualquier función personalizada que agrega sus propios encabezados WWW-Authenticate o Proxy-Authenticate, la marca [ \_ INTERNET FLAG NO \_ \_ AUTH](api-flags.md) debe establecerse para deshabilitar la autenticación.

En el ejemplo siguiente se muestra cómo se puede usar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) para controlar la autenticación HTTP.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



En el ejemplo, dwErrorCode se usa para almacenar los errores asociados a la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completa correctamente, incluso si el servidor o proxy requiere autenticación. Cuando la marca FLAGS ERROR UI FILTER FOR ERRORS se pasa a \_ \_ \_ \_ \_ [**InternetErrorDlg,**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)la función comprueba los encabezados en busca de errores ocultos. Estos errores ocultos incluirían cualquier solicitud de autenticación. [**InternetErrorDlg muestra**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) el cuadro de diálogo adecuado para solicitar al usuario los datos necesarios. Las marcas FLAGS ERROR UI FLAGS GENERATE DATA y FLAGS ERROR UI FLAGS CHANGE OPTIONS también deben pasarse a \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**InternetErrorDlg,**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) [](appendix-a-hinternet-handles.md) de modo que la función construya la estructura de datos adecuada para el error y almacena los resultados del cuadro de diálogo en el identificador HINTERNET.

En el código de ejemplo siguiente se muestra cómo se puede controlar la autenticación [**mediante InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows SERVICIOS HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 