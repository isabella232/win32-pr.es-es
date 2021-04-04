---
title: Controlar la autenticación
description: Algunos servidores proxy y servidores requieren autenticación antes de conceder acceso a los recursos de Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078534"
---
# <a name="handling-authentication"></a>Controlar la autenticación

Algunos servidores proxy y servidores requieren autenticación antes de conceder acceso a los recursos de Internet. Las funciones WinINet admiten la autenticación de servidor y proxy para las sesiones http. La autenticación de los servidores FTP debe controlarse mediante la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Actualmente no se admite la autenticación de puerta de enlace FTP.

## <a name="about-http-authentication"></a>Acerca de la autenticación HTTP

Si se requiere autenticación, la aplicación cliente recibe un código de estado 401, si el servidor requiere autenticación, o 407, si el proxy requiere autenticación. Con el código de estado, el proxy o el servidor envía uno o varios encabezados de respuesta de autenticación: proxy-Authenticate (para la autenticación de proxy) o WWW-Authenticate (para la autenticación de servidor).

Cada encabezado de respuesta de autenticación contiene un esquema de autenticación disponible y un dominio Kerberos. Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de respuesta de autenticación. El valor de dominio Kerberos distingue entre mayúsculas y minúsculas y define un espacio de protección en el proxy o el servidor. Por ejemplo, el encabezado "WWW-Authenticate: Basic realm =" example "" sería un ejemplo de un encabezado devuelto cuando se requiere la autenticación del servidor.

La aplicación cliente que envió la solicitud puede autenticarse mediante la inclusión de un campo de encabezado de autorización con la solicitud. El encabezado Authorization contendría el esquema de autenticación y la respuesta adecuada requerida por ese esquema. Por ejemplo, el encabezado "Authorization: Basic <username: password>" se agregaría a la solicitud y se volverá a enviar al servidor si el cliente recibió el encabezado de respuesta de autenticación "WWW-Authenticate: Basic realm =" example "".

Hay dos tipos generales de esquemas de autenticación:

-   Esquema de autenticación básica, donde el nombre de usuario y la contraseña se envían en texto no cifrado al servidor.
-   Esquemas de desafío-respuesta, que permiten un formato de desafío-respuesta.

El esquema de autenticación básica se basa en el modelo que un cliente debe autenticarse con un nombre de usuario y una contraseña para cada dominio Kerberos. El servidor servicios de la solicitud si se reenvía con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.

Los esquemas de desafío-respuesta permiten una autenticación más segura. Si una solicitud requiere autenticación mediante un esquema de desafío-respuesta, el código de estado y los encabezados de autenticación adecuados se devuelven al cliente. A continuación, el cliente debe volver a enviar la solicitud con un Negotiate. El servidor devolverá un código de estado adecuado con un desafío y el cliente requeriría volver a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado.

En la tabla siguiente se enumeran los esquemas de autenticación, el tipo de autenticación, el archivo DLL que los admite y una descripción del esquema.



| Scheme                                    | Tipo               | Archivo DLL                  | Descripción                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto no cifrado)                         | basic              | Wininet.dll          | Utiliza una cadena codificada en Base64 que contiene el nombre de usuario y la contraseña.                                                                                                                                                                                                                                                                             |
| Digest                                    | desafío-respuesta | Digest.dll           | Un esquema de desafío-respuesta que desafía el uso de un valor de nonce (cadena de datos especificada por el servidor). Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor de nonce dado, el método HTTP y el identificador uniforme de recursos (URI) solicitado. La compatibilidad con la autenticación implícita se presentó en Microsoft Internet Explorer 5. |
| NT LAN Manager (NTLM)                     | desafío-respuesta | Winsspi.dll          | Un esquema de desafío-respuesta que basa el desafío en el nombre de usuario.                                                                                                                                                                                                                                                                             |
| Microsoft Network (MSN)                   | desafío-respuesta | Msnsspc.dll          | Esquema de autenticación de The Microsoft Network.                                                                                                                                                                                                                                                                                                     |
| Autenticación de contraseña distribuida (DPA) | desafío-respuesta | Msapsspc.dll         | Similar a la autenticación de MSN y también la usa la red de Microsoft.                                                                                                                                                                                                                                                                           |
| Autenticación de frase de contraseña remota (RPA)    | CompuServe         | Rpawinet.dll, da.dll | Esquema de autenticación de CompuServe. Para obtener más información, vea las [Especificaciones del mecanismo RPA](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Para cualquier cosa que no sea la autenticación básica, se deben configurar las claves del registro además de instalar el archivo DLL adecuado.

Si se requiere autenticación, se debe usar la marca de la marca de [Internet \_ \_ mantener \_ conexión](api-flags.md) en la llamada a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). La marca de INTERNET \_ marcar \_ mantener \_ conexión es necesaria para NTLM y otros tipos de autenticación con el fin de mantener la conexión mientras se completa el proceso de autenticación. Si no se mantiene la conexión, el proceso de autenticación debe reiniciarse con el proxy o el servidor.

Las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completan correctamente incluso cuando se requiere autenticación. La diferencia es que los datos devueltos en los archivos de encabezado y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) recibiría una página HTML que informa al usuario del código de estado.

### <a name="registering-authentication-keys"></a>Registrar claves de autenticación

\_ \_ La preconfiguración de tipo abierto de Internet \_ examina los valores del registro **ProxyEnable**, **ProxyServer** y **ProxyOverride**. Estos valores se encuentran en **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

En el caso de los esquemas de autenticación distintos de Basic, se debe agregar una clave al registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Un valor **DWORD** , **Flags**, debe establecerse con el valor adecuado. En la lista siguiente se muestran los posibles valores para el valor **Flags** .

-   Marcas de autenticación de COMPLEMENTOs \_ \_ \_ \_ contexto único \_ por \_ TCPIP (valor = 0x01)

    Cada socket de protocolo de control de transmisión/Protocolo de Internet (TCP/IP) contiene un contexto diferente. De lo contrario, se pasa un nuevo contexto para cada plantilla de URL de bloque o dominio Kerberos.

-   Las marcas de autenticación de COMPLEMENTOs \_ \_ \_ pueden \_ controlar la interfaz de \_ usuario (valor = 0x02)

    Este archivo DLL puede administrar su propia entrada de usuario.

-   Las marcas de autenticación de COMPLEMENTOs \_ \_ \_ pueden \_ controlar \_ no \_ passwd (valor = 0x04)

    Es posible que este archivo DLL sea capaz de realizar una autenticación sin pedir al usuario una contraseña.

-   Marcas de autenticación de COMPLEMENTOs \_ \_ \_ no \_ dominio Kerberos (valor = 0x08)

    Este archivo DLL no utiliza una cadena de dominio Kerberos estándar. Los datos que parezcan ser un dominio Kerberos son datos específicos del esquema.

-   Marcas de autenticación de COMPLEMENTOs \_ \_ \_ Keep \_ Alive \_ no \_ necesaria (valor = 0x10)

    Este archivo DLL no requiere una conexión persistente para su secuencia de desafío-respuesta.

Por ejemplo, para agregar la autenticación NTLM, se debe agregar la clave NTLM a **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. En **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, se debe agregar el valor de cadena, **DLLFile**, y un valor **DWORD** , **Flags**. **DLLFile** debe establecerse en Winsspi.dll y las **marcas** deben establecerse en 0x08.

### <a name="server-authentication"></a>Autenticación de servidor

Cuando un servidor recibe una solicitud que requiere autenticación, el servidor devuelve un mensaje de código de estado 401. En ese mensaje, el servidor debe incluir uno o varios WWW-Authenticate encabezados de respuesta. Estos encabezados incluyen los métodos de autenticación que el servidor tiene disponible. WinINet elige el primer método que reconoce.

La autenticación básica proporciona una seguridad débil a menos que el canal esté cifrado primero con SSL o PCT.

La función [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada para obtener los datos.

Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer la [ \_ \_ contraseña](option-flags.md) de la opción de Internet y los valores de nombre de usuario de la [ \_ opción \_ de Internet](option-flags.md) y, a continuación, volver a enviar la solicitud al servidor.

### <a name="proxy-authentication"></a>Autenticación de proxy

Cuando un cliente intenta usar un proxy que requiere autenticación, el proxy devuelve un mensaje de código de estado 407 al cliente. En ese mensaje, el proxy debe incluir uno o varios Proxy-Authenticate encabezados de respuesta. Estos encabezados incluyen los métodos de autenticación disponibles en el proxy. WinINet elige el primer método que reconoce.

La función [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) se puede usar para obtener los datos de nombre de usuario y contraseña del usuario, o bien se puede diseñar una interfaz de usuario personalizada.

Una interfaz personalizada puede usar la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para establecer la [ \_ contraseña del \_ proxy \_](option-flags.md) de la opción de Internet y los valores de nombre de usuario del proxy de la opción de Internet y volver a enviar la solicitud al proxy. [ \_ \_ \_](option-flags.md)

Si no se establece ningún nombre de usuario y contraseña de proxy, WinINet intenta usar el nombre de usuario y la contraseña para el servidor. Este comportamiento permite a los clientes implementar la misma interfaz de usuario personalizada que se usa para controlar la autenticación de servidor.

## <a name="handling-http-authentication"></a>Control de la autenticación HTTP

La autenticación HTTP se puede controlar con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o con una función personalizada que usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o agrega sus propios encabezados de autenticación. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) puede examinar los encabezados asociados a un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) para buscar errores ocultos, como códigos de estado de un servidor proxy o un servidor. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) se puede usar para establecer el nombre de usuario y la contraseña para el proxy y el servidor. Para la autenticación de MSN y DPA, se debe usar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) para establecer el nombre de usuario y la contraseña.

En cualquier función personalizada que agregue sus propios encabezados WWW-Authenticate o Proxy-Authenticate, se debe establecer la marca [Internet \_ Flag \_ no \_ auth](api-flags.md) en deshabilitar la autenticación.

En el ejemplo siguiente se muestra cómo se puede usar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) para controlar la autenticación http.


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



En el ejemplo, dwErrorCode se usa para almacenar los errores asociados a la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se completa correctamente, aunque el proxy o el servidor requieran autenticación. Cuando la \_ \_ \_ marca marcar la interfaz \_ de usuario de error para \_ errores se pasa a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), la función comprueba si hay errores ocultos en los encabezados. Estos errores ocultos incluyen cualquier solicitud de autenticación. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) muestra el cuadro de diálogo adecuado para solicitar al usuario los datos necesarios. Las marcas de interfaz de usuario de errores de marcas \_ \_ \_ \_ generan \_ datos y marcas los indicadores \_ de la \_ interfaz de usuario de errores marcas \_ de IU \_ \_ de cambios también se deben pasar a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), para que la función construya la estructura de datos apropiada para el error y almacene los resultados del cuadro de diálogo en el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .

En el ejemplo de código siguiente se muestra cómo se puede controlar la autenticación mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


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
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 