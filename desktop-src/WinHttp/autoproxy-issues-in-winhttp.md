---
description: Tenga en cuenta los siguientes problemas importantes al usar la característica de proxy automático WinHTTP.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problemas de AutoProxy en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c6edbf56ec1ffc4dfac930a5d4858429cc6447
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580673"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problemas de AutoProxy en WinHTTP

Tenga en cuenta los siguientes problemas importantes al usar la característica de proxy automático WinHTTP.

## <a name="only-one-proxy-server-is-currently-supported"></a>Actualmente solo se admite un servidor proxy

WinHTTP no admite actualmente configuraciones de proxy que especifiquen más de un servidor proxy. Si [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) devuelve una estructura DE INFORMACIÓN DE [**PROXY WINHTTP \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene una lista de servidores proxy, que la aplicación establece en el identificador de solicitud mediante la opción **PROXY WINHTTP \_ OPTION, \_** WinHTTP solo usa el primer servidor proxy de la lista. Si ese servidor proxy no es accesible, WinHTTP no conmuta por error a ninguno de los demás servidores proxy de la lista. Depende de la aplicación controlar este caso estableciendo de nuevo la opción **\_ \_ WINHTTP OPTION PROXY** con el siguiente servidor proxy de la lista y reenlazando la solicitud.

## <a name="security-risk-mitigation"></a>Mitigación de riesgos de seguridad

El procesamiento del archivo de configuración automática del proxy requiere la ejecución del código de script descargado. Algunos problemas de seguridad que se deben tener en cuenta: si el servidor en el que reside el archivo PAC se ha puesto en peligro, es posible que el código de script PAC sea malintencionado. Por lo tanto, WinHTTP usa las precauciones siguientes para proteger el cliente:

1.  Se impide que el código de script cree instancias de ActiveX objetos. Esto bloquea una gran cantidad de funcionalidades potencialmente peligrosas, como la capacidad de acceder a archivos y realizar E/S de red.
2.  **Windows Server 2003: **[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delega todo el procesamiento de WPAD en un servicio externo fuera de proceso, el servicio de detección automática de proxy web WinHTTP, que se ejecuta en la cuenta de usuario integrada del servicio local con pocos privilegios.

3.  **Windows XP con SP2 y Windows Server 2003:** No se permite que un script PAC se ejecute durante más de 60 segundos, después de lo cual se finaliza la ejecución del script.

4.  **Windows XP con SP2 y Windows Server 2003:** WinHTTP rechaza los archivos PAC de más de 1 MB. Normalmente, un archivo PAC típico no tiene más de unos kilobytes de tamaño.

Tenga en cuenta que el procesamiento del código de script PAC requiere el uso de COM, ya que WinHTTP usa microsoft JScript componente para ejecutar el script. Si WinHTTP no puede delegar el procesamiento del protocolo WPAD en un servicio externo de detección automática de proxy web fuera de proceso, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) carga el tiempo de ejecución COM dentro del proceso de aplicación mientras dure la llamada. Si la propia aplicación ya usa COM, esto no debería ser un problema.

## <a name="performance-considerations"></a>Consideraciones de rendimiento

El proceso de detección automática puede ser lento, posiblemente hasta varios segundos. Las [**funciones WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) [y WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) están bloqueando funciones sincrónicas. Podría ser que un mecanismo de detección automática determinado (como DHCP) es mucho más lento que el otro (como DNS). Si se especifican las marcas **\_ \_ \_ \_ WINHTTP AUTO DETECT TYPE DHCP** y **WINHTTP AUTO DETECT TYPE \_ \_ DNS \_ \_ \_ A** se especifican marcas de detección automática, WinHTTP usa DHCP en primer lugar, de acuerdo con la especificación de WPAD. Si no se detecta ninguna dirección URL de PAC mediante la emisión de una solicitud DHCP, WinHTTP intenta localizar el archivo PAC en una dirección DNS conocida.

[**WinHttpGetProxyForUrl usa**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) el parámetro de identificador de sesión WinHTTP para almacenar en caché el archivo PAC y los resultados de la detección automática. Es mejor usar el mismo identificador de sesión para varias **llamadas WinHttpGetProxyForUrl** si es posible para evitar la detección repetida de direcciones URL de PAC y la descarga de archivos. El archivo PAC solo se almacena en caché en memoria y se descarta cuando la aplicación cierra el identificador de sesión.

Debido al impacto en el rendimiento del proxy automático, se recomienda que solo las aplicaciones cliente de escritorio o los servicios usen la característica. las aplicaciones basadas en servidor deben basarse en el administrador del servidor mediante la utilidad "ProxyCfg.exe".

 

 



