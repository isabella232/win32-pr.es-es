---
title: Cómo establece el cliente una conexión
description: Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f57fdc08a33c526d0bcc913a87d31d1e4a7c326bac4f17e92f53b7293e2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020835"
---
# <a name="how-the-client-establishes-a-connection"></a>Cómo establece el cliente una conexión

Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace. Una vez hecho esto, la biblioteca en tiempo de ejecución rpc busca el equipo que hospeda el programa de servidor. A continuación, busca el punto de conexión al que escucha el programa de servidor y dirige la llamada a él. En el siguiente diagrama se muestra este proceso.

![un cliente rpc establece una conexión con un servidor rpc](images/clntcon.png)

En esta sección se presenta información sobre cómo el cliente se conecta al programa de servidor y ejecuta los procedimientos remotos que ofrece. Hay muchos enfoques para completar estos pasos. en función del diseño elegido, una aplicación puede elegir un conjunto de pasos diferente. Este ejemplo es simplemente una manera de hacerlo.

La discusión se divide en las secciones siguientes:

-   [Crear un identificador de enlace](creating-a-binding-handle.md)
-   [Realización de una llamada a procedimiento remoto](making-a-remote-procedure-call.md)
-   [Buscar el programa de servidor](finding-the-server-program.md)
-   [Envío de la llamada al programa de servidor](sending-the-call-to-the-server-program.md)

 

 




