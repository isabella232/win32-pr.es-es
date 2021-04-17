---
description: En este tema se explica el uso de la herramienta de configuración de proxy de servicios HTTP de Microsoft Windows (WinHTTP) &\# 0034; ProxyCfg.exe&\# 0034;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe y ProxyCfg.exe proxy Herramientas de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539795"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe y ProxyCfg.exe proxy Herramientas de configuración

* * Windows Vista y Windows Server 2008: * *

ProxyCfg.exe ha quedado en desuso. Se reemplaza por los comandos [ winhttpNetsh.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) .

En este tema se explica el uso de la herramienta de configuración de proxy de [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md) , "ProxyCfg.exe".

Hay dos maneras de tener acceso a los servidores HTTP y el protocolo seguro de transferencia de hipertexto (HTTPS) a través de un proxy mediante los servicios HTTP de Microsoft Windows (WinHTTP). En primer lugar, puede especificar la configuración de proxy desde la aplicación WinHTTP. En segundo lugar, puede especificar la configuración de proxy predeterminada desde fuera de la aplicación mediante la utilidad de configuración de proxy ubicada en el directorio% WINDIR% \\ system32.

Puede establecer mediante programación los datos de proxy desde dentro de la aplicación o el script. Si está escribiendo una aplicación mediante la API de WinHTTP, utilice una de las dos técnicas siguientes para cambiar la configuración del proxy.

-   Utilice la función [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . Especifique el tipo de acceso en el segundo parámetro, el nombre del proxy en el tercer parámetro y una lista de omisiones en el cuarto parámetro. En el ejemplo siguiente se muestra cómo se puede usar la función [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) para establecer los datos de proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Utilice la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) . La marca de [**\_ \_ proxy de la opción WinHTTP**](option-flags.md) permite especificar la configuración de proxy con una estructura de [**\_ \_ información de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) . En el ejemplo de código siguiente se muestra cómo se puede usar la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer datos de proxy.

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

Si está escribiendo un script o una aplicación con el objeto [**WinHttpRequest**](winhttprequest.md) , utilice la siguiente técnica para cambiar la configuración del proxy.

-   Use el método [**SetProxy**](iwinhttprequest-setproxy.md) . Especifique el tipo de acceso en el primer parámetro, el nombre del proxy en el segundo parámetro y una lista de omisiones en el tercer parámetro. En el ejemplo siguiente se muestra cómo se puede usar el método [**SetProxy**](iwinhttprequest-setproxy.md) en el script para establecer los datos de proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Para especificar la configuración predeterminada y eliminar la necesidad de usar el método [**SetProxy**](iwinhttprequest-setproxy.md) o la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , use la utilidad de configuración de proxy. Con esta utilidad, puede especificar que la aplicación tenga acceso directo a una red, a través de un proxy o a través de una combinación de acceso directo y proxy especificando una lista de omisión. Cuando se usa la API de WinHTTP, la herramienta de configuración de proxy solo determina la configuración cuando se pasa la marca predeterminada de tipo de acceso de WinHTTP a la API de [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . **\_ \_ \_** El objeto [**WinHttpRequest**](winhttprequest.md) utiliza de forma predeterminada la configuración de la herramienta de configuración de proxy.

La configuración de proxy para WinHTTP no es la configuración de proxy para Microsoft Internet Explorer. No se puede establecer la configuración de proxy para WinHTTP en el panel de control de Microsoft Windows. El uso de la utilidad de configuración del proxy WinHTTP no modifica los valores de configuración que se usan en Internet Explorer.

> [!Note]  
> Si intenta abrir y enviar una solicitud HTTP con WinHTTP y la configuración del proxy no es correcta, se produce un error.

 

## <a name="command-line-parameters"></a>Parámetros de la línea de comandos

En la tabla siguiente se enumeran los parámetros de línea de comandos disponibles para su uso con la herramienta ProxyCfg.exe.



| Parámetro | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno      | Cuando no se especifica ningún parámetro, se muestra la configuración actual del proxy WinHTTP.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Se muestra la información de ayuda.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Especifica que las aplicaciones WinHTTP acceden directamente a la red, sin un proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Especifica el servidor proxy. También puede especificar una lista opcional de servidores a los que se tiene acceso sin un proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Especifica que las aplicaciones WinHTTP utilizan la configuración de proxy del usuario actual para Internet Explorer. Este parámetro no funciona si Internet Explorer detecta automáticamente la configuración de proxy o si usa una dirección URL de configuración automática para establecer la información de proxy.                                                                                                                                                      |
| i         | Especifica que las aplicaciones WinHTTP utilizan la configuración de proxy del usuario actual para Internet Explorer. Esto solo funciona cuando no se ha usado anteriormente ProxyCfg.exe. Si ProxyCfg.exe está instalado, especifique que el parámetro de línea de comandos "u" use la configuración manual. Este parámetro no funciona si Internet Explorer detecta automáticamente la configuración de proxy o si usa una dirección URL de configuración automática para establecer la información de proxy. |



 

Puede especificar servidores proxy en una cadena delimitada por espacios. Las listas de servidores proxy pueden contener el número de puerto que se usa para tener acceso al proxy. Para enumerar un proxy para un protocolo concreto, la cadena debe seguir el formato, <protocol> = https://<\_ nombre del proxy>. Los protocolos válidos son HTTP y HTTPS. Por ejemplo, para mostrar un proxy HTTP, una cadena válida es http = https://http\_proxy\_name:80 , donde \_ \_ nombre del proxy HTTP es el nombre del servidor proxy y 80 es el número de puerto que debe usar para tener acceso al proxy. Si el proxy usa el número de puerto predeterminado para ese Protocolo, puede omitir el número de puerto. Si un nombre de proxy se enumera por sí mismo, puede usarlo como el proxy predeterminado para los protocolos que no tengan un proxy especificado. Por ejemplo, http = https://http\_proxy otro \_ proxy usa \_ el proxy http para cualquier operación http, mientras que el protocolo HTTPS usa el proxy denominado otro \_ proxy.

Puede enumerar los nombres de host conocidos localmente o las direcciones IP en la lista de omisión de proxy. Esta lista puede contener caracteres comodín, como " \* ", que hacen que la aplicación omita el servidor proxy para las direcciones que se ajustan al patrón especificado, por ejemplo, " \* . Microsoft.com" o " \* . org". Los caracteres comodín deben ser los caracteres del extremo izquierdo de la lista. Por ejemplo \* , "AAA". no se admite. Para enumerar varias direcciones y nombres de host, sepárelos por espacios en blanco o punto y coma en la cadena de omisión del proxy. Si especifica la <local> macro, la función omite cualquier nombre de host que no contenga un punto.

> [!WARNING]
> Una vez que se ejecuta Proxycfg.exe, no se puede restaurar la configuración de proxy anterior. Sin embargo, puede quitar la configuración de proxy por completo.

 

## <a name="usage"></a>Uso

Para usar la herramienta de configuración de proxy, abra una ventana del símbolo del sistema y ejecute la utilidad de configuración de proxy con los parámetros de línea de comandos adecuados. En la siguiente sección se proporcionan ejemplos de sintaxis.

## <a name="example-syntax"></a>Sintaxis de ejemplo

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Ejemplo 1: usar un proxy solo para recursos externos

El siguiente es el uso más común de Proxycfg.exe. Este comando especifica que se tiene acceso a los servidores HTTP y HTTPS a través del servidor proxy denominado " \_ servidor proxy", excepto los nombres de host que no contienen un punto.

**Proxycfg-p \_ servidor proxy " <local> "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Ejemplo 2: usar un proxy para todos los recursos

En el ejemplo siguiente se especifica que se tiene acceso a los servidores HTTP y HTTPS a través del servidor proxy denominado " \_ servidor proxy". No se ha especificado ninguna lista de omisiones.

**Proxycfg-p \_ servidor proxy**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Ejemplo 3: usar un proxy diferente para proteger recursos

En el ejemplo siguiente se especifica que se tiene acceso a los servidores HTTP a través del proxy de \_ proxy http y se obtiene acceso a los servidores https a través del \_ proxy HTTPS. Los sitios de la Intranet local y cualquier sitio del \* dominio. Microsoft.com omiten el proxy.

**Proxycfg-p "http = \_ proxy http https = \_ proxy HTTPS" " <local> ; \* . microsoft.com "**

## <a name="removing-proxycfgexe"></a>Quitar ProxyCfg.exe

Después de usar la herramienta de configuración de proxy, no puede restaurar la configuración de proxy original. Sin embargo, si es necesario, puede quitar la configuración del registro que crea la utilidad. Para quitar las entradas del registro que crea ProxyCfg.exe, debe eliminar el valor de **WinHttpSettings** de la siguiente clave del registro.

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings** \\ **Connections** \\ **WinHttpSettings**

Al eliminar el valor de *WinHttpSettings* se quitan todas las configuraciones de proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe y autenticación

La utilidad de configuración de proxy establece la Directiva de autenticación predeterminada. Dado que no se debe realizar la autenticación NTLM con hosts que no son de confianza, de forma predeterminada, la autenticación NTLM solo se produce automáticamente con los hosts de la lista de omisión de proxy. Si no hay ningún proxy, todavía puede usar ProxyCfg.exe para especificar una lista de omisión de hosts en los que confíe para realizar la autenticación NTLM. Se requiere un nombre de proxy al usar ProxyCfg.exe para este propósito, pero puede usar cualquier cadena válida en lugar de un nombre de proxy real.

Para obtener más información acerca de la Directiva de inicio de sesión automático, vea [Directiva de inicio de sesión automático](authentication-in-winhttp.md).

 

 
