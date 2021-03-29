---
title: Cómo el cliente establece una conexión
description: Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075839"
---
# <a name="how-the-client-establishes-a-connection"></a>Cómo el cliente establece una conexión

Para establecer una sesión de comunicación cliente/servidor con un programa de servidor, las aplicaciones cliente con identificadores explícitos deben crear un identificador de enlace. Después de hacerlo, la biblioteca en tiempo de ejecución de RPC busca el equipo que hospeda el programa de servidor de. A continuación, busca el punto de conexión al que está escuchando el programa de servidor y dirige la llamada a él. En el siguiente diagrama se muestra este proceso.

![un cliente RPC establece una conexión con un servidor RPC](images/clntcon.png)

En esta sección se ofrece información acerca de cómo el cliente se conecta al programa de servidor y ejecuta los procedimientos remotos que ofrece. Existen muchos enfoques para completar estos pasos: en función del diseño elegido, una aplicación puede elegir un conjunto de pasos diferente. Este ejemplo es simplemente una forma de hacerlo.

La discusión se divide en las siguientes secciones:

-   [Crear un controlador de enlace](creating-a-binding-handle.md)
-   [Realización de una llamada a procedimiento remoto](making-a-remote-procedure-call.md)
-   [Buscar el programa de servidor](finding-the-server-program.md)
-   [Enviar la llamada al programa de servidor](sending-the-call-to-the-server-program.md)

 

 




