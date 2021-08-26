---
title: Envío de la llamada al programa de servidor
description: Una vez que el tiempo de ejecución de RPC del lado cliente se ha conectado al punto de conexión del servidor, programa los argumentos y los envía al servidor.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Procedimiento remoto Llame a RPC , tareas, enviando la llamada al servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a02d4fc1d69ba45cc6de3d43fba62724de1277471992790e3098225f579d305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017915"
---
# <a name="sending-the-call-to-the-server-program"></a>Envío de la llamada al programa de servidor

Una vez que el tiempo de ejecución de RPC del lado cliente se ha conectado al punto de conexión del servidor, programa los argumentos y los envía al servidor. El tiempo de ejecución DE RPC del servidor proporciona los argumentos de marshalled al código auxiliar que los desmarca y, a continuación, los pasa a las rutinas del servidor. Cuando se devuelven las rutinas del servidor, el código auxiliar recoge los parámetros out y \[ \] \[ in,out, y el valor devuelto, los programa y envía los datos de salida al tiempo de ejecución RPC del \] servidor. El tiempo de ejecución de RPC devuelve los datos al cliente, donde el tiempo de ejecución rpc del cliente los entrega al código auxiliar del lado cliente que los desmarta y los devuelve al autor de la llamada.

 

 




