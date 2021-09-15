---
title: Requisitos del sistema RPC sobre HTTP, interoperabilidad
description: Rpc de Microsoft admite RPC sobre HTTP, como se muestra en la tabla siguiente.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476598"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisitos del sistema RPC sobre HTTP, interoperabilidad

Rpc de Microsoft admite RPC sobre HTTP, como se muestra en la tabla siguiente.



| Plataforma                             | Es compatible con                       | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clientes, servidores y proxy RPC | Admite RPC a través de HTTP v1 y RPC a través de cliente y servidor HTTP v2. El proxy RPC admite RPC sobre HTTP v2 cuando IIS se ejecuta en modo IIS 6.0. El proxy RPC admite RPC sobre HTTP v1 y RPC sobre HTTP v2 cuando IIS se ejecuta en modo IIS 5.0. Sin embargo, no se recomienda ejecutar en modo IIS 5.0. Para [más información,](rpc-over-http-deployment-recommendations.md) consulte RPC a través Recomendaciones implementación http. RPC a través del servidor HTTP y el proxy RPC pueden estar en equipos diferentes. |
| Windows XP con Service Pack 1 (SP1) | Clientes y servidores            | Admite RPC a través de HTTP v1 y RPC a través de cliente y servidor HTTP v2. No admite el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clientes y servidores            | Solo admite RPC a través de cliente y servidor HTTP v1. No admite el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clientes, servidores y proxy RPC | El programa de servidor RPC a través de HTTP y el proxy RPC se pueden ejecutar en equipos diferentes. RPC sobre el cliente HTTP, el servidor y el proxy RPC solo admiten RPC a través de HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Además, se aplican los siguientes requisitos:

-   Windows 2000 y versiones posteriores requieren el uso de IIS 4.0 o posterior.
-   El proxy RPC a través de HTTP solo Windows ediciones de servidor.
-   Si IIS se ejecuta en una versión de servidor de Windows, el programa de servidor RPC a través de HTTP se puede ejecutar en cualquier equipo al que el proxy RPC esté configurado para reenviar el tráfico. Por lo tanto, se puede ejecutar en el mismo equipo que el proxy RPC o en otro equipo.

Para que se establezca una conexión RPC a través de HTTP, todas las RPC a través del cliente HTTP, el servidor RPC a través de HTTP y el proxy RPC deben coincidir en qué versión de RPC sobre HTTP se usa. Si no hay ninguna versión común de RPC a través de HTTP que las tres admitan (cliente, servidor y proxy RPC), no se puede establecer una conexión RPC a través de HTTP. En la tabla siguiente se resume esta interoperabilidad para diferentes versiones de RPC a través de HTTP.



| RPC sobre el cliente HTTP | RPC Proxy      | RPC sobre servidor HTTP | ¿Obras?                                      | Versión usada     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| Solo v1              | Solo v1        | Solo v1              | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| Solo v1              | Solo v1        | V1 y v2       | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| Solo v1              | V1 y v2 | Solo v1              | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| Solo v1              | V1 y v2 | V1 y v2       | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| Solo v1              | Solo v2        | Solo v1              | No                                          |                  |
| Solo v1              | Solo v2        | V1 y v2       | No                                          |                  |
| V1 y v2       | Solo v1        | Solo v1              | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| V1 y v2       | Solo v1        | V1 y v2       | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| V1 y v2       | V1 y v2 | Solo v1              | Sí, con limitaciones de v1                    | RPC sobre HTTP v1 |
| V1 y v2       | V1 y v2 | V1 y v2       | Sí                                         | RPC sobre HTTP v2 |
| V1 y v2       | Solo v2        | Solo v1              | No                                          |                  |
| V1 y v2       | Solo v2        | V1 y v2       | Sí. Esta es la configuración recomendada. | RPC sobre HTTP v2 |



 

Por ejemplo, imagine un cliente Windows 2000, un proxy de Windows Server 2003 con IIS que se ejecuta en modo IIS 6.0 y un servidor RPC de Windows Server 2003 sobre HTTP. La primera tabla de esta página de referencia muestra que Windows 2000 solo admite RPC sobre HTTP v1. La misma tabla revela que un servidor Windows Server 2003 con IIS que se ejecuta en modo IIS 6.0 solo admite RPC sobre HTTP v2 y que un servidor RPC sobre HTTP de Windows Server 2003 admite RPC sobre HTTP v1 y RPC sobre HTTP v2. Este escenario se describe en la fila 6 de la segunda tabla de esta página de referencia, donde se muestra que no se puede establecer una conexión RPC a través de HTTP. Además, la segunda tabla revela que existen dos opciones para ese escenario:

-   Si la seguridad y la solidez no son una consideración, IIS se puede cambiar al modo IIS 5.0, donde admite RPC sobre HTTP v1 y RPC sobre HTTP v2. Si lo hace, se habilitaría el establecimiento de una conexión RPC a través de HTTP v1.
-   Actualice el cliente Windows 98 a Windows XP con SP1 y obtenga la eficacia, la seguridad y la solidez de una conexión RPC a través de HTTP v2.

 

 




