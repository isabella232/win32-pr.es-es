---
title: Cómo se prepara el servidor para una conexión
description: Cuando se inicia la ejecución de un programa de servidor, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357259"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Cómo se prepara el servidor para una conexión

Cuando se inicia la ejecución de un programa de servidor, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC. A continuación, crea la información de enlace necesaria. El programa de servidor también debe registrar el punto de conexión o los puntos de conexión a los que escucha. Después, puede empezar a escuchar las llamadas de cliente. Este proceso se ilustra en el diagrama siguiente.

![una aplicación de servidor RPC se prepara para las conexiones de cliente](images/srvrcon.png)

En función del diseño elegido, una aplicación de servidor puede elegir un conjunto diferente de pasos; en el ejemplo anterior y en la ilustración se ofrece un enfoque.

En esta sección se ofrece información acerca de los pasos que debe realizar un proceso de servidor para preparar una conexión. La discusión se divide en las siguientes secciones:

-   [Registrar la interfaz](registering-the-interface.md)
-   [Poner el servidor a disposición en la red](making-the-server-available-on-the-network.md)
-   [Registro de puntos de conexión](registering-endpoints.md)
-   [Escuchando llamadas de cliente](listening-for-client-calls.md)

 

 




