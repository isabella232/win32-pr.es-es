---
title: Conexión del cliente y el servidor
description: Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Llamada a procedimiento remoto RPC, tareas, conexión de cliente y servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f477802ffb4b72f33ce951bf811b1cb9b770a8272f646507dfaa450934569f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931232"
---
# <a name="connecting-the-client-and-the-server"></a>Conexión del cliente y el servidor

Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan. Una vez que establece la conexión, el cliente puede llamar a procedimientos remotos en el programa de servidor como si fueran locales para el programa cliente.

En esta sección se proporciona información general conceptual sobre cómo establecer una conexión entre clientes y servidores para llamadas a procedimientos remotos. No proporciona una explicación detallada de este tema. Todos los conceptos de esta sección se presentan en detalle en capítulos posteriores y en la sección Referencia de función RPC.

La discusión presentada en esta sección se divide en los temas siguientes:

-   [Terminología esencial del enlace RPC](essential-rpc-binding-terminology.md)
-   [Cómo se prepara el servidor para una conexión](how-the-server-prepares-for-a-connection.md)
-   [Cómo establece el cliente una conexión](how-the-client-establishes-a-connection.md)

Tenga en cuenta que la explicación supone identificadores de enlace explícitos. Sin embargo, si la aplicación usa otros tipos de identificadores de enlace, es posible que tenga que modificar los pasos presentados en esta sección. Para obtener más información, vea [Enlace y identificadores](binding-and-handles.md).

 

 




