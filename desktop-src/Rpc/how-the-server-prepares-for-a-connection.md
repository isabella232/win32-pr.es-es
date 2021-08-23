---
title: Cómo se prepara el servidor para una conexión
description: Cuando un programa de servidor comienza la ejecución, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66314c55ad8e78922f7afcc74c6de3b4afad8234293373cf0cd35a560a1942ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929502"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Cómo se prepara el servidor para una conexión

Cuando un programa de servidor comienza la ejecución, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución de RPC. A continuación, crea la información de enlace necesaria. El programa de servidor también debe registrar el punto de conexión o los puntos de conexión a los que escucha. A continuación, puede empezar a escuchar las llamadas de cliente. Este proceso se ilustra en el diagrama siguiente.

![una aplicación de servidor rpc se prepara para las conexiones de cliente](images/srvrcon.png)

En función del diseño elegido, una aplicación de servidor puede elegir un conjunto de pasos diferente. El ejemplo y la ilustración anteriores proporcionan un enfoque.

En esta sección se presenta información sobre los pasos que debe seguir un proceso de servidor para prepararse para una conexión. La discusión se divide en las secciones siguientes:

-   [Registro de la interfaz](registering-the-interface.md)
-   [Hacer que el servidor esté disponible en la red](making-the-server-available-on-the-network.md)
-   [Registro de puntos de conexión](registering-endpoints.md)
-   [Escucha de llamadas de cliente](listening-for-client-calls.md)

 

 




