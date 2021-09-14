---
title: Cómo se prepara el servidor para una conexión
description: Cuando un programa de servidor comienza la ejecución, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución rpc.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244677"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Cómo se prepara el servidor para una conexión

Cuando un programa de servidor comienza la ejecución, primero debe registrar la interfaz o las interfaces que contiene con la biblioteca en tiempo de ejecución rpc. A continuación, crea la información de enlace necesaria. El programa de servidor también debe registrar el punto de conexión o los puntos de conexión en los que escucha. A continuación, puede empezar a escuchar las llamadas de cliente. Este proceso se ilustra en el diagrama siguiente.

![una aplicación de servidor rpc se prepara para las conexiones de cliente](images/srvrcon.png)

En función del diseño elegido, una aplicación de servidor puede elegir un conjunto de pasos diferente; El ejemplo y la ilustración anteriores proporcionan un enfoque.

En esta sección se presenta información sobre los pasos que debe seguir un proceso de servidor para prepararse para una conexión. La discusión se divide en las secciones siguientes:

-   [Registro de la interfaz](registering-the-interface.md)
-   [Hacer que el servidor esté disponible en la red](making-the-server-available-on-the-network.md)
-   [Registro de puntos de conexión](registering-endpoints.md)
-   [Escucha de llamadas de cliente](listening-for-client-calls.md)

 

 




