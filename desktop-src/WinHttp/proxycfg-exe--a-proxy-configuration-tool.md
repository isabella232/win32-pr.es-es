---
description: En este tema se explica el uso de la herramienta de configuración de proxy de servicios HTTP de Microsoft Windows (WinHTTP), &\# 0034;ProxyCfg.exe&\# 0034;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe y ProxyCfg.exe proxy Herramientas de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64c952db59fb4709614c498b4d9c732403798e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885831"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe y ProxyCfg.exe proxy Herramientas de configuración

**Windows Vista y Windows Server 2008: **

ProxyCfg.exe ha quedado en desuso. Se reemplaza por losNetsh.exe [comandos winhttp.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10))

En este tema se explica el uso de la herramienta [de configuración de proxy Windows HTTP Services (WinHTTP)](about-winhttp.md) de Microsoft, "ProxyCfg.exe".

Hay dos maneras de acceder a los servidores HTTP y protocolo de transferencia de hipertexto seguro (HTTPS) a través de un proxy mediante los servicios HTTP de Microsoft Windows (WinHTTP). En primer lugar, puede especificar la configuración del proxy desde dentro de la aplicación WinHTTP. En segundo lugar, puede especificar la configuración de proxy predeterminada desde fuera de la aplicación mediante la utilidad de configuración de proxy que se encuentra en el directorio %windir% \\ system32.

Puede establecer mediante programación los datos de proxy desde la aplicación o el script. Si va a escribir una aplicación mediante la API WinHTTP, use una de las dos técnicas siguientes para cambiar la configuración del proxy.

-   Use la [**función WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) Especifique el tipo de acceso en el segundo parámetro, el nombre del proxy en el tercer parámetro y una lista de omisión en el cuarto parámetro. En el ejemplo siguiente se muestra cómo se puede usar la función [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) para establecer datos de proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Use la [**función WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) La [**marca WINHTTP \_ OPTION \_ PROXY**](option-flags.md) le permite especificar la configuración del proxy con una [**estructura DE INFORMACIÓN DE \_ \_ PROXY WINHTTP.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) El código de ejemplo siguiente muestra cómo se puede usar la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer datos de proxy.

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

Si va a escribir un script o una aplicación mediante el [**objeto WinHttpRequest,**](winhttprequest.md) use la siguiente técnica para cambiar la configuración del proxy.

-   Use el [**método SetProxy.**](iwinhttprequest-setproxy.md) Especifique el tipo de acceso en el primer parámetro, el nombre del proxy en el segundo parámetro y una lista de omisión en el tercer parámetro. En el ejemplo siguiente se muestra cómo se puede usar [**el método SetProxy**](iwinhttprequest-setproxy.md) en el script para establecer datos de proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Para especificar la configuración predeterminada y eliminar la necesidad de usar el método [**SetProxy**](iwinhttprequest-setproxy.md) o la función [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) use la utilidad de configuración de proxy. Con esta utilidad, puede especificar que la aplicación acceda a una red directamente, a través de un proxy o a través de una combinación de acceso directo y proxy especificando una lista de omisión. Cuando se usa la API WinHTTP, la herramienta de configuración de proxy solo determina la configuración cuando se pasa la marca **WINHTTP \_ ACCESS TYPE \_ \_ DEFAULT** a la API [**WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) El [**objeto WinHttpRequest**](winhttprequest.md) usa la configuración de la herramienta de configuración de proxy de forma predeterminada.

La configuración de proxy para WinHTTP no es la configuración de proxy para Microsoft Internet Explorer. No se pueden configurar las opciones de proxy para WinHTTP en microsoft Windows Panel de control. El uso de la utilidad de configuración de proxy WinHTTP no modifica la configuración que se usa para Internet Explorer.

> [!Note]  
> Si intenta abrir y enviar una solicitud HTTP mediante WinHTTP y la configuración del proxy es incorrecta, se produce un error.

 

## <a name="command-line-parameters"></a>Parámetros de la línea de comandos

En la tabla siguiente se enumeran los parámetros de línea de comandos disponibles para su uso con ProxyCfg.exe herramienta.



| Parámetro | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno      | Cuando no se especifica ningún parámetro, se muestra la configuración actual del proxy WinHTTP.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Se muestra la información de ayuda.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Especifica que las aplicaciones WinHTTP acceden a la red directamente, sin un proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Especifica el servidor proxy. También puede especificar una lista opcional de servidores a los que se accede sin un proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Especifica que las aplicaciones WinHTTP usan la configuración de proxy del usuario actual para Internet Explorer. Este parámetro no funciona si Internet Explorer detecta automáticamente la configuración del proxy o si usa una dirección URL de configuración automática para establecer la información del proxy.                                                                                                                                                      |
| i         | Especifica que las aplicaciones WinHTTP usan la configuración de proxy del usuario actual para Internet Explorer. Esto solo funciona cuando ProxyCfg.exe no se usó anteriormente. Si ProxyCfg.exe está instalado, especifique que el parámetro de línea de comandos "u" use la configuración manual. Este parámetro no funciona si Internet Explorer automáticamente la configuración del proxy o si usa una dirección URL de configuración automática para establecer la información del proxy. |



 

Puede especificar servidores proxy en una cadena delimitada por espacios. Las listas de proxy pueden contener el número de puerto que se usa para acceder al proxy. Para enumerar un proxy para un protocolo específico, la cadena debe seguir el formato &lt; protocolo &gt; =https://<nombre de proxy \_>. Los protocolos válidos son HTTP y HTTPS. Por ejemplo, para enumerar un proxy HTTP, una cadena válida es http= , donde el nombre del proxy http es el nombre del servidor proxy y 80 es el número de puerto que debe usar para acceder al https://http\_proxy\_name:80 \_ \_ proxy. Si el proxy usa el número de puerto predeterminado para ese protocolo, puede omitir el número de puerto. Si un nombre de proxy aparece por sí solo, puede usarlo como proxy predeterminado para cualquier protocolo que no tenga un proxy especificado. Por ejemplo, http= otro proxy usa el proxy HTTP para cualquier operación HTTP, mientras que el protocolo HTTPS usa https://http\_proxy el proxy denominado otro \_ \_ \_ proxy.

Puede enumerar nombres de host conocidos localmente o direcciones IP en la lista de omisión de proxy. Esta lista puede contener caracteres comodín, como "", que hacen que la aplicación omita el servidor proxy para las direcciones que se ajustan al patrón especificado, por \* ejemplo, \* ".microsoft.com" o \* ".org". Los caracteres comodín deben ser los caracteres situados más a la izquierda de la lista. Por ejemplo, "aaa. \* " no se admite. Para enumerar varias direcciones y nombres de host, sepárelos por espacios en blanco o punto y coma en la cadena de omisión del proxy. Si especifica la &lt; &gt; macro local, la función omite cualquier nombre de host que no contenga un punto.

> [!WARNING]
> Después Proxycfg.exe ejecuta, no se puede restaurar la configuración de proxy anterior. Sin embargo, puede quitar completamente la configuración del proxy.

 

## <a name="usage"></a>Uso

Para usar la herramienta de configuración de proxy, abra una ventana del símbolo del sistema y ejecute la utilidad de configuración de proxy con los parámetros de línea de comandos adecuados. En la sección siguiente se proporcionan ejemplos de sintaxis.

## <a name="example-syntax"></a>Sintaxis de ejemplo

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Ejemplo 1: Uso de un proxy solo para recursos externos

A continuación se muestra el uso más común para Proxycfg.exe. Este comando especifica que se tiene acceso a los servidores HTTP y HTTPS a través del servidor proxy denominado "servidor proxy", excepto para los nombres de host que no \_ contienen un punto.

**proxycfg -p servidor proxy \_ " &lt; local &gt; "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Ejemplo 2: Uso de un proxy para todos los recursos

En el ejemplo siguiente se especifica que se tiene acceso a los servidores HTTP y HTTPS a través del servidor proxy denominado "servidor \_ proxy". No se especifica ninguna lista de omisión.

**proxycfg -p servidor \_ proxy**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Ejemplo 3: Uso de un proxy diferente para recursos seguros

En el ejemplo siguiente se especifica que se tiene acceso a los servidores HTTP a través del proxy http y se accede a los servidores \_ HTTPS a través del proxy \_ https. Los sitios de intranet locales y cualquier sitio del \* dominio .microsoft.com omiten el proxy.

**proxycfg -p "http=http \_ proxy https=https \_ proxy" " &lt; local ; &gt; \* . microsoft.com"**

## <a name="removing-proxycfgexe"></a>Quitar ProxyCfg.exe

Después de usar la herramienta de configuración de proxy, no puede restaurar la configuración de proxy original. Sin embargo, si es necesario, puede quitar la configuración del Registro que crea la utilidad . Para quitar las entradas del Registro que ProxyCfg.exe crea, debe eliminar el **valor WinHttpSettings** de la siguiente clave del Registro.

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Configuración** \\ **Connections** \\ **WinHttpSettings**

Al eliminar el *valor WinHttpSettings* se quitan todas las configuraciones de proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe y autenticación

La utilidad de configuración de proxy establece la directiva de autenticación predeterminada. Dado que no debe realizar la autenticación NTLM con hosts que no son de confianza, de forma predeterminada, la autenticación NTLM solo se produce automáticamente con hosts en la lista de omisión del proxy. Si no hay ningún proxy, puede seguir utilizando ProxyCfg.exe especificar una lista de hosts de omisión en los que confíe para realizar la autenticación NTLM. Se requiere un nombre de proxy al ProxyCfg.exe para este fin, pero puede usar cualquier cadena válida en lugar de un nombre de proxy real.

Para obtener más información sobre la directiva de inicio de sesión automático, vea [Directiva de inicio de sesión automático.](authentication-in-winhttp.md)

 

 
