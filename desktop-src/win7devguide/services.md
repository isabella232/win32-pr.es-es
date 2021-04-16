---
title: Servicios (guía para desarrolladores de Windows 7)
description: Windows 7 proporciona una plataforma eficaz, muy extensible y administrable para crear e integrar los servicios web y las aplicaciones del futuro. Windows 7 ofrece API de código administrado y API nativas para compilar y ejecutar servicios Web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aab84cbb522f21b9a09a85d80ef25bf1c858baf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685812"
---
# <a name="services-windows-7-developer-guide"></a>Servicios (guía para desarrolladores de Windows 7)

Windows 7 proporciona una plataforma eficaz, muy extensible y administrable para crear e integrar los servicios web y las aplicaciones del futuro.

Windows 7 ofrece API de código administrado y API nativas para compilar y ejecutar servicios Web. Una variedad de características nuevas se basa en una nueva capa de extensibilidad que permite a los desarrolladores extender todas las API, en código nativo o en el marco de Microsoft .NET.

Windows 7 también permite a los desarrolladores aprovechar las mejores capacidades de almacenamiento en caché y búsqueda. Con estas mejoras, los desarrolladores pueden recuperar datos más rápido y reducir el uso de ancho de banda de red.

## <a name="windows-web-services"></a>Servicios Web de Windows

Con los [servicios Web de Windows](/windows/desktop/wsw/portal), puede crear aplicaciones que se comuniquen fácilmente con un equipo local o un servicio Web remoto. Servicios Web de Windows es una implementación de código nativo de SOAP y proporciona la comunicación de red principal, ya que admite un amplio conjunto de la familia de protocolos de servicios web (*WS*). Servicios Web de Windows es un elemento del mismo nivel que [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, servicios Web de código administrado) y proporciona un subconjunto de alto rendimiento de la funcionalidad de *WCF* . Servicios Web de Windows proporciona las siguientes ventajas:

-   La capacidad de compilar servicios Web de código nativo en C/C++ en el cliente y el servidor de Windows.
-   Amplia integración con servicios de [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) .
-   La capacidad de compilar servicios web con un tiempo mínimo de inicio.
-   La capacidad de compilar servicios en función de la familia de protocolos principales de *WS* y los estándares del *W3C* .
-   La capacidad de usar servicios web en entornos con restricción de recursos.

Para obtener más información, consulte [API de servicios Web de Windows](../wsw/portal.md) e implementación de servicios Web [con la API de servicios Web de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabla de enrutamiento distribuido

Windows 7 facilita la creación de sofisticadas aplicaciones punto a punto, como sistemas de archivos distribuidos y redes de distribución de contenido, con la [tabla de enrutamiento distribuida](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). La tabla de enrutamiento distribuida proporciona un mecanismo seguro y escalable para publicar y buscar claves en un sistema punto a punto. Se puede usar para crear tablas hash distribuidas y construir topologías para redes de superposición. (Consulte [enrutamiento distribuido Table API](../p2psdk/distributed-routing-table-api.md)).

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 mejora la capacidad de respuesta de las aplicaciones entre servidores centrales y equipos de sucursales. En las redes actuales, la comunicación entre los servidores centrales y las sucursales a menudo se congestiona, lo que da lugar a un rendimiento más lento en las aplicaciones de la sucursal. Con Windows BranchCache, los clientes pueden recuperar datos de otros clientes en su propia rama que ya han descargado los datos, en lugar de tener que recuperar los datos a través de servidores remotos. Como resultado, el tráfico de vínculos de red de área extensa (WAN) disminuye y mejora la capacidad de respuesta de la aplicación. La caché conserva una copia de todo el contenido que los clientes de la bifurcación han solicitado y garantiza que solo los clientes autorizados por el servidor de contenido puedan acceder a los datos solicitados, a la vez que conservan el cifrado de un extremo a otro de los datos.

Windows BranchCache ya está integrado con HTTP y bloque de mensajes del servidor (SMB). Si una aplicación usa WindowsAPIs para cualquiera de estos protocolos, Windows BranchCache puede ayudar a aumentar el rendimiento de esta aplicación en Windows 7 sin realizar ningún cambio en ella.

Si la aplicación recupera los mismos datos varias veces desde un servidor a través de un vínculo WAN y no se optimiza automáticamente con Windows 7, es fácil usar el BranchCacheAPIs de Windows para optimizar la aplicación para que funcione más rápido en Windows 7 y satisfaga a los usuarios de la sucursal.

Estas nuevas características ayudan a reducir el tráfico WAN y la latencia, a la vez que garantizan el cumplimiento de las normas de seguridad. (Consulte [distribución del mismo nivel](../p2psdk/peer-distribution.md)).

 

 
