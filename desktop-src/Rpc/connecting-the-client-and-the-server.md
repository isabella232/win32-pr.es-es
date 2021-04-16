---
title: Conexión del cliente y el servidor
description: Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- RPC llamada a procedimiento remoto, tareas, conexión de cliente y servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486858"
---
# <a name="connecting-the-client-and-the-server"></a>Conexión del cliente y el servidor

Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan. Una vez que se establece la conexión, el cliente puede llamar a procedimientos remotos en el programa de servidor como si fueran locales para el programa cliente.

En esta sección se proporciona información conceptual sobre cómo establecer una conexión entre clientes y servidores para llamadas a procedimientos remotos. No proporciona una explicación detallada de este tema. Todos los conceptos de esta sección se presentan en detalle en los capítulos posteriores y en la sección de referencia de la función RPC.

La discusión presentada en esta sección se divide en los temas siguientes:

-   [Terminología de enlace RPC esencial](essential-rpc-binding-terminology.md)
-   [Cómo se prepara el servidor para una conexión](how-the-server-prepares-for-a-connection.md)
-   [Cómo el cliente establece una conexión](how-the-client-establishes-a-connection.md)

Tenga en cuenta que en la discusión se asumen los identificadores de enlace explícitos. Sin embargo, si la aplicación usa otros tipos de identificadores de enlace, es posible que tenga que modificar los pasos que se presentan en esta sección. Para obtener más información, vea [enlazar y controlar](binding-and-handles.md).

 

 




