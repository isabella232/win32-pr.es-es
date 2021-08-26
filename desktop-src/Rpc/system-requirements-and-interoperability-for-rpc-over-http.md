---
title: Requisitos del sistema RPC sobre HTTP, interoperabilidad
description: Rpc de Microsoft admite RPC a través de HTTP, como se muestra en la tabla siguiente.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc9019789821499168a76d4d2e02ef485529e08b99c5f0759a19bfb4a46f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017315"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisitos del sistema RPC sobre HTTP, interoperabilidad

Rpc de Microsoft admite RPC a través de HTTP, como se muestra en la tabla siguiente.



| Plataforma                             | Es compatible con                       | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clientes, servidores y proxy RPC | Admite RPC a través de HTTP v1 y RPC sobre cliente y servidor HTTP v2. El proxy RPC admite RPC a través de HTTP v2 cuando IIS se ejecuta en modo IIS 6.0. El proxy RPC admite RPC sobre HTTP v1 y RPC sobre HTTP v2 cuando IIS se ejecuta en modo IIS 5.0. Sin embargo, no se recomienda ejecutar en modo IIS 5.0. Para [más información, consulte](rpc-over-http-deployment-recommendations.md) RPC a través de Recomendaciones http. El servidor RPC a través de HTTP y el proxy RPC pueden estar en equipos diferentes. |
| Windows XP con Service Pack 1 (SP1) | Clientes y servidores            | Admite RPC a través de HTTP v1 y RPC sobre cliente y servidor HTTP v2. No admite el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clientes y servidores            | Solo admite RPC a través de cliente y servidor HTTP v1. No admite el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clientes, servidores y proxy RPC | El programa de servidor RPC a través de HTTP y el proxy RPC se pueden ejecutar en equipos diferentes. Rpc a través del cliente HTTP, el servidor y el proxy RPC solo admiten RPC a través de HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Además, se aplican los siguientes requisitos:

-   Windows 2000 y versiones posteriores requieren el uso de IIS 4.0 o posterior.
-   El proxy RPC a través de HTTP se ejecuta Windows solo en ediciones de servidor.
-   Si IIS se ejecuta en una versión de servidor de Windows, el programa de servidor RPC a través de HTTP se puede ejecutar en cualquier equipo al que el proxy RPC esté configurado para reenviar el tráfico. Por lo tanto, se puede ejecutar en el mismo equipo que el proxy RPC o en otro equipo.

Para que se establezca una conexión RPC a través de HTTP, todas las RPC sobre el cliente HTTP, el servidor RPC a través de HTTP y el proxy RPC deben coincidir en qué versión de RPC a través de HTTP se usa. Si no hay ninguna versión común de RPC a través de HTTP que admitan los tres (cliente, servidor y proxy RPC), no se puede establecer una conexión RPC a través de HTTP. En la tabla siguiente se resume esta interoperabilidad para diferentes versiones de RPC a través de HTTP.



| CLIENTE RPC a través de HTTP | RPC Proxy      | RPC a través del servidor HTTP | ¿Obras?                                      | Versión usada     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| Solo v1              | Solo v1        | Solo v1              | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| Solo v1              | Solo v1        | V1 y v2       | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| Solo v1              | V1 y v2 | Solo v1              | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| Solo v1              | V1 y v2 | V1 y v2       | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| Solo v1              | Solo v2        | Solo v1              | No                                          |                  |
| Solo v1              | Solo v2        | V1 y v2       | No                                          |                  |
| V1 y v2       | Solo v1        | Solo v1              | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| V1 y v2       | Solo v1        | V1 y v2       | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| V1 y v2       | V1 y v2 | Solo v1              | Sí, con limitaciones de v1                    | RPC a través de HTTP v1 |
| V1 y v2       | V1 y v2 | V1 y v2       | Sí                                         | RPC a través de HTTP v2 |
| V1 y v2       | Solo v2        | Solo v1              | No                                          |                  |
| V1 y v2       | Solo v2        | V1 y v2       | Sí. Esta es la configuración recomendada. | RPC a través de HTTP v2 |



 

Por ejemplo, imagine un cliente Windows 2000, un proxy de Windows Server 2003 con IIS que se ejecuta en modo IIS 6.0 y un servidor RPC sobre HTTP de Windows Server 2003. La primera tabla de esta página de referencia muestra que Windows 2000 solo admite RPC sobre HTTP v1. La misma tabla revela que un servidor Windows Server 2003 con IIS que se ejecuta en modo IIS 6.0 solo admite RPC sobre HTTP v2 y que un servidor RPC sobre HTTP de Windows Server 2003 admite RPC sobre HTTP v1 y RPC sobre HTTP v2. Este escenario se describe en la fila 6 de la segunda tabla de esta página de referencia, donde se muestra que no se puede establecer una conexión RPC a través de HTTP. Además, la segunda tabla revela que existen dos opciones para ese escenario:

-   Si la seguridad y la solidez no son una consideración, IIS se puede cambiar al modo IIS 5.0, donde admite RPC sobre HTTP v1 y RPC sobre HTTP v2. Si lo hace, se habilitaría el establecimiento de una conexión RPC a través de HTTP v1.
-   Actualice el cliente Windows 98 a Windows XP con SP1 y obtenga la potencia, la seguridad y la solidez de una conexión RPC a través de HTTP v2.

 

 




