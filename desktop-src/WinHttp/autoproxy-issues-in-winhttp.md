---
description: Tenga en cuenta los siguientes problemas importantes al usar la característica de AutoProxy WinHTTP.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problemas de AutoProxy en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c6edbf56ec1ffc4dfac930a5d4858429cc6447
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278420"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problemas de AutoProxy en WinHTTP

Tenga en cuenta los siguientes problemas importantes al usar la característica de AutoProxy WinHTTP.

## <a name="only-one-proxy-server-is-currently-supported"></a>Actualmente solo se admite un servidor proxy

WinHTTP no admite actualmente configuraciones de proxy que especifiquen más de un servidor proxy. Si [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) devuelve una estructura de [**\_ \_ información del proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene una lista de servidores proxy, que la aplicación establece entonces en el identificador de solicitud mediante la opción de **\_ \_ proxy WinHTTP Option** , WinHTTP usa solo el primer servidor proxy de la lista. Si no se puede tener acceso a ese servidor proxy, WinHTTP no conmutará por error a ninguno de los demás servidores proxy de la lista. Depende de la aplicación controlar este caso estableciendo de nuevo la opción del **\_ \_ proxy WinHTTP Option** con el siguiente servidor proxy de la lista y reenviando la solicitud.

## <a name="security-risk-mitigation"></a>Mitigación del riesgo de seguridad

El procesamiento del archivo de configuración automática del proxy requiere la ejecución del código de script descargado. Algunos aspectos de seguridad que se deben tener en cuenta: Si el servidor en el que reside el archivo PAC está en peligro, es posible que el código de script PAC sea malintencionado. Por lo tanto, WinHTTP usa las siguientes precauciones para proteger el cliente:

1.  Se impide que el código de script Cree instancias de objetos ActiveX. Esto bloquea una gran cantidad de funcionalidad potencialmente peligrosa, como la capacidad de obtener acceso a los archivos y realizar la e/s de red.
2.  * * Windows Server 2003: * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delega todo el procesamiento de WPAD en un servicio externo fuera de proceso, el servicio de detección automática de proxy web WinHTTP, que se ejecuta en la cuenta de usuario integrada del servicio local con pocos privilegios.

3.  **Windows XP con SP2 y Windows Server 2003:** No se permite que un script de PAC se ejecute durante más de 60 segundos, después de la finalización de la ejecución del script.

4.  **Windows XP con SP2 y Windows Server 2003:** WinHTTP rechaza los archivos PAC de más de 1 MB. Un archivo PAC típico no suele tener más de unos pocos kilobytes de tamaño.

Tenga en cuenta que el procesamiento del código de script PAC requiere el uso de COM, porque WinHTTP usa el componente de Microsoft JScript para ejecutar el script. Si WinHTTP no puede delegar el procesamiento del protocolo WPAD a un servicio externo de detección automática de proxy Web fuera de proceso, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) carga el tiempo de ejecución de com en el proceso de la aplicación mientras dure la llamada. Si la propia aplicación ya usa COM, no debería ser un problema.

## <a name="performance-considerations"></a>Consideraciones de rendimiento

El proceso de detección automática puede ser lento, posiblemente en varios segundos. Las funciones [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) están bloqueando las funciones sincrónicas. Podría ser que un mecanismo de detección automática determinado (como DHCP) es mucho más lento que el otro (como DNS). Si el tipo de detección automática de WinHTTP es tipo de detección automática de **\_ \_ \_ \_ DHCP** y WinHTTP, se especifican marcas de detección automática de **\_ \_ \_ \_ DNS \_** , WinHTTP usará primero DHCP, de acuerdo con la especificación de WPAD. Si no se detecta ninguna dirección URL de PAC mediante la emisión de una solicitud DHCP, WinHTTP intentará localizar el archivo PAC en una dirección DNS conocida.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) usa el parámetro de identificador de sesión de WinHTTP para almacenar en caché el archivo PAC y los resultados de la detección automática. Es mejor usar el mismo identificador de sesión para varias llamadas **WinHttpGetProxyForUrl** , si es posible, para evitar la detección de archivos y la detección de direcciones URL de PAC repetidas. El archivo PAC se almacena en caché únicamente en memoria y se descarta cuando la aplicación cierra el identificador de sesión.

Debido al impacto en el rendimiento de AutoProxy, se recomienda que solo los servicios o aplicaciones cliente de escritorio usen la característica; las aplicaciones basadas en servidor deben confiar en el administrador del servidor mediante la utilidad "ProxyCfg.exe".

 

 



