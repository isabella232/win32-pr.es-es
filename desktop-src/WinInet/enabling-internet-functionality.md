---
title: Habilitar la funcionalidad de Internet
description: Antes de utilizar las funciones de WinINet, la aplicación debe intentar realizar una conexión a Internet mediante la función InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb44fadaf0726b81618dde19105da7517673a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078235"
---
# <a name="enabling-internet-functionality"></a>Habilitar la funcionalidad de Internet

Antes de utilizar las funciones de WinINet, la aplicación debe intentar realizar una conexión a Internet mediante la función [**InternetAttemptConnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) . Esta función llama al cuadro de diálogo de acceso telefónico para iniciar una conexión a Internet o comprobar si ya existe una conexión. Si se produce un error en esta función, la aplicación puede entrar en el modo sin conexión, lo que le permite tener acceso a la información almacenada en caché durante las conexiones anteriores a Internet.

Utilice la función [**InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) para comprobar la conexión a Internet. Intenta hacer ping en el servidor designado por la dirección URL que se pasa a la función. Si se establece la marca de conexión de la fuerza ICC de la marca \_ \_ \_ y la dirección URL es **null**, la función comprueba si hay una entrada en la base de datos del servidor para el servidor más cercano. Si existe, la función hace ping a ese servidor.

A continuación, utilice la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para establecer las características de la conexión a Internet que utiliza la aplicación cliente. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) crea el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz que se usa para establecer las sesiones [http](http-sessions.md)[FTP](ftp-sessions.md) . [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) no prueba la conexión a Internet para comprobar que las características que se pasan a la función son correctas.

Utilice la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para crear una sesión específica. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Inicializa una sesión para el sitio especificado usando los argumentos que se le pasan y crea un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que es una bifurcación del identificador raíz. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no intenta tener acceso o establecer una conexión con el sitio especificado, excepto en el caso de una sesión de FTP. Las funciones [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)y [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan el identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para establecer una conexión con el sitio especificado.

## <a name="using-internetopen"></a>Usar InternetOpen

Para habilitar una conexión a Internet, se debe crear un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) raíz con [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Información sobre el agente de usuario (la aplicación que llama a las funciones de Internet), el tipo de acceso a Internet, los nombres de proxy, los hosts y direcciones que omiten el proxy, y el comportamiento se pasa a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Establecimiento del agente de usuario

La aplicación que realiza la llamada debe proporcionar una cadena que contenga el nombre de la aplicación o entidad que tiene acceso a Internet al parámetro *lpszAgent* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Esta cadena se utiliza como agente de usuario en el protocolo HTTP. Por ejemplo, Microsoft Internet Explorer usa "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Establecimiento de tipos de acceso

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) admite tres tipos de acceso:

-   Usar \_ el tipo abierto de Internet \_ \_ directo si el sistema en el que se ejecuta la aplicación utiliza una conexión directa a Internet. Los parámetros *lpszProxyName* y *lpszProxyBypass* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) no se usan y deben establecerse en **null**.
-   Usar \_ \_ proxy de tipo abierto de Internet \_ si el sistema en el que se ejecuta la aplicación utiliza uno o varios servidores proxy para tener acceso a Internet. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa los servidores proxy indicados por *lpszProxyName* y omite el proxy para cualquier nombre de host o dirección IP especificada por *lpszProxyBypass*.
-   Utilice \_ \_ preconfiguración de tipo abierto de Internet \_ para indicar a la aplicación que debe recuperar la configuración del registro. Esta suele ser la mejor opción, ya que la mayoría de las aplicaciones, incluidos los exploradores Web, usan esta opción.

\_ \_ La preconfiguración de tipo abierto de Internet \_ examina los valores del registro **ProxyEnable**, **ProxyServer** y **ProxyOverride**. Estos valores se encuentran en "HKEY \_ Current \_ User \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings".

Si **ProxyEnable** es cero, la aplicación usa el \_ tipo abierto de Internet \_ \_ Direct. De lo contrario, la aplicación \_ usa \_ el proxy de tipo abierto de Internet \_ y usa la información de **ProxyServer** y **ProxyOverride** .

Las funciones WinINet solo proporcionan compatibilidad con los servidores proxy de tipo SOCKS si está instalado Internet Explorer. La instalación de Internet Explorer incluye el archivo de Wsock32n.dll, que es necesario para admitir servidores proxy de SOCKS. Wsock32n.dll no es redistribuible.

### <a name="listing-proxy-servers"></a>Enumerar servidores proxy

WinINet reconoce dos tipos de proxies: servidores proxy de tipo CERN (sólo HTTP) y proxy de proxy TIS (solo FTP). Si Internet Explorer está instalado, WinINet también admite servidores proxy de tipo SOCKS. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) supone, de forma predeterminada, que el proxy especificado es un proxy CERN. Si el tipo de acceso se establece en \_ Internet \_ Open \_ Type Direct o en Internet \_ Open \_ Type \_ Preconfig, el parámetro *LpszProxyName* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) debe establecerse en **null**. De lo contrario, el valor pasado a *lpszProxyName* debe contener los proxies en una cadena delimitada por espacios. Las listas de servidores proxy pueden contener el número de puerto que se usa para tener acceso al proxy.

Para enumerar un proxy para un protocolo concreto, la cadena debe seguir el formato "" <protocol> <protocol> ://<\_ nombre del proxy> "". Los protocolos válidos son HTTP, HTTPS y FTP. Por ejemplo, para mostrar un proxy FTP, una cadena válida sería "" FTP = FTP://FTP \_ proxy \_ Name: 21 "", donde \_ \_ nombre del proxy FTP es el nombre del proxy FTP y 21 es el número de puerto que se debe usar para tener acceso al proxy. Si el proxy usa el número de puerto predeterminado para ese Protocolo, se puede omitir el número de puerto. Si un nombre de proxy se enumera por sí mismo, se usa como el proxy predeterminado para los protocolos que no tienen especificado un proxy específico. Por ejemplo, "http = https://http\_proxy other" "usaría el proxy HTTP \_ para cualquier operación http, mientras que todos los demás protocolos usarían otros.

De forma predeterminada, la función supone que el proxy especificado por *lpszProxyName* es un proxy CERN. Una aplicación puede especificar más de un proxy, incluidos distintos servidores proxy para los diferentes protocolos. Por ejemplo, si especifica "FTP = FTP://FTP-GW HTTP = https://jericho:99 proxy" ", las solicitudes FTP se realizan a través del proxy FTP-GW, que escucha en el puerto 21, y las solicitudes HTTP se realizan a través de un proxy CERN denominado Jericho, que escucha en el puerto 99. De lo contrario, las solicitudes HTTP se realizarían a través del proxy de CERN denominado proxy, que escucha en el puerto 80. Tenga en cuenta que si la aplicación solo usa FTP, por ejemplo, no es necesario especificar "FTP = FTP://FTP-GW: 21" ". Podría especificar solo "" FTP-GW "". Una aplicación solo es necesaria para especificar los nombres de Protocolo si usa más de un protocolo por identificador devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Mostrar la omisión del proxy

Los nombres de host o direcciones IP que no se deben enviar al proxy pueden aparecer en la lista de omisión de proxy. Esta lista puede contener caracteres comodín, " \* ", que hacen que la aplicación omita el servidor proxy para las direcciones que se ajustan al patrón especificado. Para enumerar varias direcciones y nombres de host, sepárelos con punto y coma en la cadena de omisión del proxy. Si <local> se especifica la macro "", la función omite el proxy para cualquier nombre de host que no contenga un punto.

De forma predeterminada, WinINet omitirá el proxy para las solicitudes que usan los nombres de host "localhost", "loopback", "127.0.0.1" o " \[ :: 1 \] ". Este comportamiento existe porque un servidor proxy remoto no suele resolver correctamente estas direcciones.

**Internet Explorer 9:** Puede quitar el equipo local de la lista de omisión de proxy mediante la macro "<-loopback>".

En el ejemplo siguiente se muestran llamadas de ejemplo a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) con diferentes cadenas de omisión de proxy. Los comentarios anteriores a cada llamada describen el efecto que tiene la cadena de omisión en los nombres de host a los que se tiene acceso desde el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que crea.


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>Usar InternetConnect

Para iniciar una sesión, la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe crear un identificador del identificador raíz devuelto por la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) establece la dirección del servidor, el número de puerto, el nombre de usuario, la contraseña y el tipo de servicio.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para establecer un identificador de sesión. Si se estableció la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), la llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe incluir un valor de contexto distinto de cero.

El nombre de servidor puede contener el nombre de host (por ejemplo, "www.servername.com") o el número de IP del sitio en formato decimal con puntos ASCII (por ejemplo, "10.0.1.45").

El puerto del servidor es el número de puerto del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) para conectarse a en el servidor. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa el puerto predeterminado para el tipo de servicio seleccionado si \_ se usa el valor de número de puerto no válido de Internet \_ \_ . Las tablas siguientes contienen los valores predeterminados del puerto del servidor para WinINet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>INTERNET_DEFAULT_FTP_PORT</td>
<td>Use el puerto predeterminado para los servidores FTP (puerto 21).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_GOPHER_PORT</td>
<td>Use el puerto predeterminado para los servidores Gopher (puerto 70).
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Use el puerto predeterminado para los servidores HTTP (puerto 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Use el puerto predeterminado para los servidores https (puerto 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Use el puerto predeterminado para los servidores de Firewall SOCKS (puerto 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definir el nombre de usuario y la contraseña

El valor de *lpszUsername* es la dirección de una cadena terminada en **null** que contiene el nombre del usuario que está iniciando sesión. Si este parámetro es **null**, la función utiliza un valor predeterminado adecuado, excepto http. Un parámetro **null** en http hace que el servidor devuelva un error. Para el protocolo FTP, el valor predeterminado es Anonymous.

El valor de *lpszPassword* es la dirección de una cadena terminada en **null** que contiene la contraseña de inicio de sesión. Si *lpszUsername* y *lpszPassword* son **null**, la función usa la contraseña anónima predeterminada. En el caso de FTP, la contraseña anónima predeterminada es el nombre de correo electrónico del usuario. Si *lpszUsername* no es **null** y *lpszPassword* es **null**, la función utiliza una contraseña en blanco. Hay cuatro valores posibles de *lpszUsername* y *lpszPassword*, que generan los comportamientos que se muestran en la tabla siguiente.



| *lpszUsername*      | *lpszPassword*      | Nombre de usuario enviado al servidor FTP | Contraseña enviada al servidor FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | Anonymous                  | Nombre de correo electrónico del usuario           |
| Cadena que no es **null** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Cadena que no es **null** | ERROR                        | ERROR                       |
| Cadena que no es **null** | Cadena que no es **null** | *lpszUsername*               | *lpszPassword*              |



 

Esta información se puede cambiar mediante las funciones [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) . [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) cambia los valores de nombre de usuario y contraseña, mientras que [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) muestra un cuadro de diálogo que solicita el nombre de usuario y la contraseña correctos.

### <a name="defining-the-session"></a>Definir la sesión

Para definir la sesión que se está estableciendo, establezca el tipo de servicio, las marcas y el valor de contexto para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

Hay dos tipos de servicio disponibles para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta): \_ \_ FTP de servicio de INTERNET y servicio de Internet \_ \_ http. El \_ servicio \_ de Internet http se usa para las sesiones http y https.

[Internet \_ de FLAG \_ passive](api-flags.md) es la única marca específica del servicio que usan las funciones de Wininet. Esta marca se puede establecer cuando el tipo de servicio es \_ \_ FTP de servicio de Internet para poder usar la semántica de FTP pasiva.

Para todas las operaciones sincrónicas, el valor de *dwContext* debe establecerse en cero. Si se establecieron operaciones asincrónicas estableciendo la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), se debe proporcionar un valor distinto de cero para *dwContext*. Para obtener más información sobre las operaciones asincrónicas, vea [configurar operaciones asincrónicas](common-functions.md).

En el caso de las sesiones FTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) intenta establecer una conexión con el servidor en Internet. En el caso de las sesiones HTTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no establece una conexión hasta que otra función intenta obtener información del servidor.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

