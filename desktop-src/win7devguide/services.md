---
title: Servicios (Windows 7 Developer Guide)
description: Windows 7 proporciona una plataforma eficaz, muy extensible y fácil de administrar para compilar e integrar los servicios web y las aplicaciones del futuro. Windows 7 ofrece API de código administrado y API nativas para compilar y ejecutar servicios web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42fe2a59a69efe7fb34bb4a09c58b2ee03f00ac8b8129c36b1ef5f0f61971c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203868"
---
# <a name="services-windows-7-developer-guide"></a>Servicios (Windows 7 Developer Guide)

Windows 7 proporciona una plataforma eficaz, muy extensible y fácil de administrar para compilar e integrar los servicios web y las aplicaciones del futuro.

Windows 7 ofrece API de código administrado y API nativas para compilar y ejecutar servicios web. Una variedad de características nuevas se basa en una nueva capa de extensibilidad que permite a los desarrolladores ampliar todas las API, en código nativo o dentro de microsoft .NET Framework.

Windows 7 también permite a los desarrolladores aprovechar las mejores funcionalidades de almacenamiento en caché y búsqueda. Con estas mejoras, los desarrolladores pueden recuperar datos con mayor rapidez y reducir el uso del ancho de banda de red.

## <a name="windows-web-services"></a>Windows Servicios web

Con [Windows Web Services](/windows/desktop/wsw/portal), puede crear aplicaciones que se comuniquen fácilmente con un equipo local o un servicio web remoto. Windows Servicios web es una implementación de código nativo de SOAP y proporciona comunicación de red principal al admitir un amplio conjunto de la familia de protocolos de servicios web *(WS).* Windows Web Services es un elemento del mismo [nivel que Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) *(WCF,* servicios web de código administrado) y proporciona un subconjunto de alto rendimiento de la *funcionalidad de WCF.* Windows Los servicios web proporcionan las siguientes ventajas:

-   La capacidad de compilar servicios web de código nativo en C/C++ en Windows cliente y servidor.
-   Amplia integración [con Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) Services.
-   La capacidad de crear servicios web con un tiempo de inicio mínimo.
-   La capacidad de crear servicios basados en la familia *WS* principal de protocolos y *estándares W3C.*
-   La capacidad de usar servicios web en entornos con recursos restringidos.

Para obtener más información, [consulte Windows WEB Services API](../wsw/portal.md) e Implement Web Services with the Windows Web Services API ( Implementar servicios web con la API Windows Web [Services).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI)

## <a name="distributed-routing-table"></a>Tabla de enrutamiento distribuido

Windows 7 facilita la compilación de sofisticadas aplicaciones punto a punto, como sistemas de archivos distribuidos y redes de distribución de contenido con la [tabla de enrutamiento distribuido](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). La tabla de enrutamiento distribuido proporciona un mecanismo seguro y escalable para publicar y buscar claves en un sistema punto a punto. Se puede usar para compilar tablas hash distribuidas y crear topologías para redes superpuestas. (Vea [Distributed Routing Table API](../p2psdk/distributed-routing-table-api.md)).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 mejora la capacidad de respuesta de la aplicación entre servidores centrales y equipos de sucursal. En las redes actuales, la comunicación entre los servidores centrales y las sucursales se suele ingerir, lo que da lugar a un rendimiento más lento para las aplicaciones de la sucursal. Con Windows BranchCache, los clientes pueden recuperar datos de otros clientes de su propia rama que ya han descargado los datos, en lugar de tener que recuperar los datos a través de servidores remotos. Como resultado, el tráfico de vínculos de red de área extensa (WAN) disminuye y mejora la capacidad de respuesta de la aplicación. La memoria caché conserva una copia de todo el contenido que los clientes de la rama han solicitado y garantiza que solo los clientes autorizados por el servidor de contenido puedan acceder a los datos solicitados, al tiempo que se conserva el cifrado de un extremo a otro de los datos.

Windows BranchCache ya está integrado con HTTP y bloque de mensajes de servidor (SMB). Si una aplicación usa WindowsAPIs para cualquiera de estos protocolos, Windows BranchCache puede ayudar a aumentar el rendimiento de esta aplicación en Windows 7 sin realizar ningún cambio en ella.

Si la aplicación recupera los mismos datos varias veces de un servidor a través de un vínculo WAN y no se optimiza automáticamente mediante Windows 7, es fácil usar los Windows BranchCacheAPIs para optimizar la aplicación para que funcione más rápido en Windows 7 y satisfacer a los usuarios de la rama.

Estas nuevas características ayudan a reducir el tráfico y la latencia de WAN, al tiempo que garantizan el cumplimiento de los requisitos de seguridad. (Vea [Distribución del mismo nivel).](../p2psdk/peer-distribution.md)

 

 
