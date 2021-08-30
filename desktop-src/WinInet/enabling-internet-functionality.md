---
title: Habilitación de la funcionalidad de Internet
description: Antes de usar las funciones de WinINet, la aplicación debe intentar realizar una conexión a Internet mediante la función InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f4c45aed970651e2bae6b6742097653f393dd9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468072"
---
# <a name="enabling-internet-functionality"></a>Habilitación de la funcionalidad de Internet

Antes de usar las funciones de WinINet, la aplicación debe intentar realizar una conexión a Internet mediante la [**función InternetAttemptConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) Esta función llama al cuadro de diálogo de acceso telefónico para iniciar una conexión a Internet o comprobar si ya existe una conexión. Si se produce un error en esta función, la aplicación puede entrar en modo sin conexión, lo que le permite acceder a la información almacenada en caché durante las conexiones anteriores a Internet.

Use la [**función InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) para comprobar la conexión a Internet. Intenta hacer ping al servidor designado por la dirección URL que se pasa a la función. Si se establece la marca FLAG ICC FORCE CONNECTION y la dirección URL es NULL, la función comprueba si hay una entrada en la base de datos del servidor para el \_ \_ servidor más \_ cercano.  Si existe, la función hace ping a ese servidor.

A continuación, use [**la función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para establecer las características de la conexión a Internet que usa la aplicación cliente. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) crea el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz que se usa para establecer [sesiones ftp http.](http-sessions.md)[](ftp-sessions.md) [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) no prueba la conexión a Internet para comprobar que las características pasadas a la función son correctas.

Use la [**función InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para crear una sesión específica. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) inicializa una sesión para el sitio especificado mediante los argumentos que se le pasan y crea un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que es una rama fuera del identificador raíz. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no intenta acceder ni establecer una conexión al sitio especificado, excepto en el caso de una sesión FTP. [**Las funciones FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)y [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan el identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para establecer una conexión al sitio especificado.

## <a name="using-internetopen"></a>Uso de InternetAbrir

Para habilitar una conexión a Internet, se debe crear un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz mediante [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Información sobre el agente de usuario (la aplicación que llama a las funciones de Internet), el tipo de acceso a Internet, los nombres de proxy, los hosts y las direcciones que omiten el proxy y el comportamiento se pasan a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Establecer el agente de usuario

La aplicación que realiza la llamada debe proporcionar una cadena que contenga el nombre de la aplicación o entidad que accede a Internet al parámetro *lpszAgent* [**de InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Esta cadena se usa como agente de usuario en el protocolo HTTP. Por ejemplo, Microsoft Internet Explorer usa "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Establecimiento de tipos de acceso

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) admite tres tipos de acceso:

-   Use INTERNET OPEN TYPE DIRECT si el sistema en el que se ejecuta la aplicación \_ usa una conexión directa a \_ \_ Internet. Los *parámetros lpszProxyName* y *lpszProxyBypass* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) no se usan y deben establecerse en **NULL.**
-   Use INTERNET OPEN TYPE PROXY si el sistema en el que se ejecuta la aplicación usa uno o varios servidores \_ proxy para acceder a \_ \_ Internet. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa los servidores proxy indicados por *lpszProxyName* y omite el proxy para los nombres de host o direcciones IP especificados por *lpszProxyBypass*.
-   Use INTERNET \_ OPEN \_ TYPE \_ PRECONFIG para indicar a la aplicación que recupere la configuración del Registro. Esta suele ser la mejor opción, ya que la mayoría de las aplicaciones, incluidos los exploradores web, usan esta opción.

INTERNET OPEN TYPE PRECONFIG examina los valores del \_ Registro \_ \_ **ProxyEnable**, **ProxyServer** y **ProxyOverride.** Estos valores se encuentran en "HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Internet \\ Configuración".

Si **ProxyEnable** es cero, la aplicación usa INTERNET \_ OPEN TYPE \_ \_ DIRECT. De lo contrario, la aplicación usa INTERNET \_ OPEN TYPE PROXY y usa la información \_ \_ **proxyServer** **y ProxyOverride.**

Las funciones de WinINet proporcionan compatibilidad con servidores proxy de tipo SOCKS solo si Internet Explorer está instalado. La instalación de Internet Explorer incluye el Wsock32n.dll, que es necesario para admitir servidores proxy SOCKS. Wsock32n.dll no es redistribuible.

### <a name="listing-proxy-servers"></a>Enumeración de servidores proxy

WinINet reconoce dos tipos de servidores proxy: servidores proxy de tipo CERN (solo HTTP) y servidores proxy DE TIS FTP (solo FTP). Si Internet Explorer instalado, WinINet también admite servidores proxy de tipo SOCKS. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) supone, de forma predeterminada, que el proxy especificado es un proxy CERN. Si el tipo de acceso se establece en INTERNET OPEN TYPE DIRECT o INTERNET OPEN TYPE PRECONFIG, el parámetro \_ \_ \_ \_ \_ \_ *lpszProxyName* [**de InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) debe establecerse en **NULL.** De lo contrario, el valor pasado *a lpszProxyName* debe contener los servidores proxy en una cadena delimitada por espacios. Las listas de proxy pueden contener el número de puerto que se usa para acceder al proxy.

Para enumerar un proxy para un protocolo específico, la cadena debe seguir el formato "" <protocol> <protocol> ://<nombre de proxy \_>"". Los protocolos válidos son HTTP, HTTPS y FTP. Por ejemplo, para enumerar un proxy FTP, una cadena válida sería ""ftp=ftp://ftp \_ proxy \_ name:21"", donde el nombre del proxy ftp es el nombre del proxy FTP y \_ 21 es el número de puerto que se debe usar para acceder \_ al proxy. Si el proxy usa el número de puerto predeterminado para ese protocolo, se puede omitir el número de puerto. Si un nombre de proxy aparece por sí solo, se usa como proxy predeterminado para los protocolos que no tienen especificado un proxy específico. Por ejemplo, ""http= other"" usaría el proxy http para cualquier operación HTTP, mientras que el resto de https://http\_proxy \_ protocolos usarían otros.

De forma predeterminada, la función supone que el proxy especificado por *lpszProxyName* es un proxy CERN. Una aplicación puede especificar más de un proxy, incluidos distintos servidores proxy para los distintos protocolos. Por ejemplo, si especifica ""ftp=ftp://ftp-gw HTTP= proxy"", las solicitudes FTP se realizan a través del proxy ftp-gw, que escucha en el puerto 21, y las solicitudes HTTP se realizan a través de un proxy CERN llamado jericho, que escucha en el https://jericho:99 puerto 99. De lo contrario, las solicitudes HTTP se realizarían a través del proxy CERN denominado proxy, que escucha en el puerto 80. Tenga en cuenta que si la aplicación solo usa FTP, por ejemplo, no tendría que especificar ""ftp=ftp://ftp-gw:21"". Podría especificar simplemente ""ftp-gw"". Una aplicación solo es necesaria para especificar los nombres de protocolo si usa más de un protocolo por identificador devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Enumeración de la omisión del proxy

Los nombres de host o las direcciones IP que no se deben enviar al proxy se pueden enumerar en la lista de omisión del proxy. Esta lista puede contener caracteres comodín, "", que hacen que la aplicación omita el servidor proxy para las direcciones que \* se ajustan al patrón especificado. Para enumerar varias direcciones y nombres de host, separelas con punto y coma en la cadena de omisión del proxy. Si se especifica la macro " ", la función omite el proxy para cualquier <local> nombre de host que no contenga un punto.

De forma predeterminada, WinINet omitirá el proxy para las solicitudes que usan los nombres de host "localhost", "loopback", "127.0.0.1" o \[ "::1". \] Este comportamiento existe porque un servidor proxy remoto normalmente no resolverá estas direcciones correctamente.

**Internet Explorer 9:** Puede quitar el equipo local de la lista de omisión de proxy mediante la macro "<-loopback>".

En el ejemplo siguiente se muestran llamadas de ejemplo [**a InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) mediante diferentes cadenas de omisión de proxy. Los comentarios anteriores a cada llamada describen el efecto que tiene la cadena de omisión en los nombres de host a los que se accede desde el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que crea.


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



## <a name="using-internetconnect"></a>Uso de InternetConnect

Para comenzar una sesión, la [**función InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe crear un identificador fuera del identificador raíz devuelto por la [**función InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) establece la dirección del servidor, el número de puerto, el nombre de usuario, la contraseña y el tipo de servicio.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para establecer un identificador de sesión. Si la [marca \_ INTERNET FLAG \_ ASYNC](api-flags.md) se estableció en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), la llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe incluir un valor de contexto distinto de cero.

El nombre de servidor puede contener el nombre de host (por ejemplo, "www.servername.com") o el número IP del sitio en formato decimal con puntos ASCII (por ejemplo, "10.0.1.45").

El puerto del servidor es el número de puerto del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) al que se va a conectar en el servidor. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa el puerto predeterminado para el tipo de servicio seleccionado si se usa el valor \_ NÚMERO DE PUERTO NO VÁLIDO DE \_ \_ INTERNET. Las tablas siguientes contienen los valores predeterminados de puerto del servidor para WinINet.




| Valor | Significado | 
|-------|---------|
| INTERNET_DEFAULT_FTP_PORT | Use el puerto predeterminado para servidores FTP (puerto 21). | 
| INTERNET_DEFAULT_GOPHER_PORT | Use el puerto predeterminado para los servidores gopher (puerto 70).<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_DEFAULT_HTTP_PORT | Use el puerto predeterminado para los servidores HTTP (puerto 80). | 
| INTERNET_DEFAULT_HTTPS_PORT | Use el puerto predeterminado para los servidores HTTPS (puerto 443). | 
| INTERNET_DEFAULT_SOCKS_PORT | Use el puerto predeterminado para los servidores de firewall de SOCKS (puerto 1080). | 




 

### <a name="defining-the-user-name-and-password"></a>Definir el nombre de usuario y la contraseña

El valor de *lpszUsername* es la dirección de una cadena terminada en **NULL** que contiene el nombre del usuario que inicia sesión. Si este parámetro es **NULL,** la función usa un valor predeterminado adecuado, excepto HTTP. Un **parámetro NULL** en HTTP hace que el servidor devuelva un error. Para el protocolo FTP, el valor predeterminado es anónimo.

El valor de *lpszPassword* es la dirección de una cadena terminada en **NULL** que contiene la contraseña de inicio de sesión. Si *lpszUsername y* *lpszPassword* son **NULL,** la función usa la contraseña anónima predeterminada. En el caso de FTP, la contraseña anónima predeterminada es el nombre de correo electrónico del usuario. Si *lpszUsername no* es **NULL** y *lpszPassword* **es NULL,** la función usa una contraseña en blanco. Hay cuatro valores posibles de *lpszUsername* y *lpszPassword,* que generan los comportamientos que se muestran en la tabla siguiente.



| *lpszUsername*      | *lpszPassword*      | Nombre de usuario enviado al servidor FTP | Contraseña enviada al servidor FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | "anonymous"                  | Nombre de correo electrónico del usuario           |
| Cadena que **no es NULL** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Cadena que **no es NULL** | ERROR                        | ERROR                       |
| Cadena que **no es NULL** | Cadena que **no es NULL** | *lpszUsername*               | *lpszPassword*              |



 

Esta información se puede cambiar mediante las [**funciones InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) [**e InternetErrorDlg.**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) [**InternetSetOption cambia**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) los valores de nombre de usuario y contraseña, mientras [**que InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) muestra un cuadro de diálogo que solicita el nombre de usuario y la contraseña adecuados.

### <a name="defining-the-session"></a>Definir la sesión

Para definir la sesión que se establece, establezca el tipo de servicio, las marcas y el valor de contexto [**para InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

Hay dos tipos de servicio disponibles para [**InternetConnect:**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) \_ INTERNET SERVICE FTP e INTERNET SERVICE \_ \_ \_ HTTP. HTTP \_ DE SERVICIO DE INTERNET se usa para sesiones HTTP y \_ HTTPS.

[INTERNET \_ FLAG \_ PASSIVE](api-flags.md) es la única marca específica del servicio que usan las funciones de WinINet. Esta marca se puede establecer cuando el tipo de servicio es FTP DE SERVICIO \_ DE INTERNET para usar la semántica de FTP \_ pasiva.

Para todas las operaciones sincrónicas, el *valor de dwContext* debe establecerse en cero. Si se establecieron operaciones asincrónicas estableciendo la marca [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), se debe proporcionar un valor distinto de cero para *dwContext*. Para obtener más información sobre las operaciones asincrónicas, vea [Configurar operaciones asincrónicas.](common-functions.md)

Para las sesiones FTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) intenta establecer una conexión al servidor en Internet. Para las sesiones HTTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no establece una conexión hasta que otra función intenta obtener información del servidor.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

