---
title: Requisitos del sistema de RPC a través de HTTP, interoperabilidad
description: Microsoft RPC admite RPC a través de HTTP, tal y como se muestra en la tabla siguiente.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104077164"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisitos del sistema de RPC a través de HTTP, interoperabilidad

Microsoft RPC admite RPC a través de HTTP, tal y como se muestra en la tabla siguiente.



| Plataforma                             | Es compatible con                       | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clientes, servidores y proxy RPC | Admite RPC a través de HTTP V1 y el cliente y el servidor RPC a través de HTTP V2. El proxy RPC admite RPC a través de HTTP V2 cuando IIS se ejecuta en modo IIS 6,0. El proxy RPC admite RPC a través de HTTP V1 y RPC a través de HTTP V2 cuando IIS se ejecuta en modo IIS 5,0. Sin embargo, no se recomienda ejecutar en modo IIS 5,0. Consulte [recomendaciones de implementación de RPC sobre http](rpc-over-http-deployment-recommendations.md) para obtener más información. El servidor RPC a través de HTTP y el proxy RPC pueden estar en equipos diferentes. |
| Windows XP con Service Pack 1 (SP1) | Clientes y servidores            | Admite RPC a través de HTTP V1 y el cliente y el servidor RPC a través de HTTP V2. No es compatible con el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clientes y servidores            | Solo es compatible con clientes y servidores de RPC a través de HTTP v1. No es compatible con el proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clientes, servidores y proxy RPC | El programa de servidor RPC a través de HTTP y el proxy RPC pueden ejecutarse en equipos diferentes. El cliente RPC a través de HTTP, el servidor y el proxy RPC solo admiten RPC a través de HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Además, se aplican los siguientes requisitos:

-   Windows 2000 y versiones posteriores requieren el uso de IIS 4,0 o posterior.
-   El proxy RPC a través de HTTP solo se ejecuta en las ediciones de Windows Server.
-   Si IIS se está ejecutando en una versión de servidor de Windows, el programa de servidor RPC a través de HTTP puede ejecutarse en cualquier equipo en el que el proxy RPC esté configurado para reenviar el tráfico. Por lo tanto, se puede ejecutar en el mismo equipo que el proxy RPC o en otro equipo.

Para que se establezca una conexión RPC a través de HTTP, todo el cliente RPC a través de HTTP, el servidor RPC a través de HTTP y el proxy RPC deben estar de acuerdo en qué versión de RPC a través de HTTP se usa. Si no hay ninguna versión común de RPC a través de HTTP que admitan las tres (cliente, servidor y proxy RPC), no se puede establecer una conexión RPC a través de HTTP. En la tabla siguiente se resume esta interoperabilidad para las distintas versiones de RPC a través de HTTP.



| Cliente RPC a través de HTTP | Proxy RPC      | Servidor RPC a través de HTTP | Válido?                                      | Versión usada     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| solo v1              | solo v1        | solo v1              | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| solo v1              | solo v1        | V1 y V2       | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| solo v1              | V1 y V2 | solo v1              | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| solo v1              | V1 y V2 | V1 y V2       | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| solo v1              | solo V2        | solo v1              | No                                          |                  |
| solo v1              | solo V2        | V1 y V2       | No                                          |                  |
| V1 y V2       | solo v1        | solo v1              | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| V1 y V2       | solo v1        | V1 y V2       | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| V1 y V2       | V1 y V2 | solo v1              | Sí, con limitaciones v1                    | RPC a través de HTTP v1 |
| V1 y V2       | V1 y V2 | V1 y V2       | Sí                                         | RPC a través de HTTP V2 |
| V1 y V2       | solo V2        | solo v1              | No                                          |                  |
| V1 y V2       | solo V2        | V1 y V2       | Sí. Esta es la configuración recomendada. | RPC a través de HTTP V2 |



 

Por ejemplo, Imagine un cliente de Windows 2000, un proxy de Windows Server 2003 con IIS que se ejecute en modo IIS 6,0 y un servidor RPC de Windows Server 2003 RPC sobre HTTP. La primera tabla de esta página de referencia muestra que Windows 2000 solo es compatible con RPC sobre HTTP v1. En la misma tabla se revela que un servidor de Windows 2003 con IIS que se ejecuta en modo de IIS 6,0 solo admite RPC a través de HTTP V2 y que un servidor de RPC a través de http de Windows Server 2003 admite RPC a través de http V1 y RPC a través de HTTP V2. Este escenario se describe en la fila 6 de la segunda tabla de esta página de referencia, donde se muestra que no se puede establecer una conexión RPC a través de HTTP. Además, la segunda tabla revela que existen dos opciones para ese escenario:

-   Si no se tiene en cuenta la seguridad y la solidez, IIS se puede cambiar al modo IIS 5,0, donde es compatible con RPC a través de HTTP V1 y RPC a través de HTTP V2. Esto permitiría el establecimiento de una conexión RPC a través de HTTP v1.
-   Actualice el cliente de Windows 98 a Windows XP con SP1 y obtenga la eficacia, seguridad y solidez de una conexión RPC a través de HTTP V2.

 

 




