---
title: Enviar la llamada al programa de servidor
description: Una vez que el tiempo de ejecución de RPC del cliente se ha conectado al punto de conexión del servidor, calcula las referencias de los argumentos y los envía al servidor.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- RPC llamada a procedimiento remoto, tareas y envío de la llamada al servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357549"
---
# <a name="sending-the-call-to-the-server-program"></a>Enviar la llamada al programa de servidor

Una vez que el tiempo de ejecución de RPC del cliente se ha conectado al punto de conexión del servidor, calcula las referencias de los argumentos y los envía al servidor. El tiempo de ejecución de RPC del servidor proporciona al código auxiliar los argumentos de cálculo de referencias que los elimina y, a continuación, los pasa a las rutinas de servidor. Cuando se devuelven las rutinas de servidor, el código auxiliar recoge los \[ \] parámetros out y \[ in, out \] y el valor devuelto, los calcula de las referencias y envía los datos de cálculo de referencias al tiempo de ejecución de RPC del servidor. El tiempo de ejecución de RPC envía los datos de vuelta al cliente, donde el tiempo de ejecución de RPC del cliente los entrega al código auxiliar del lado cliente que los quita y los devuelve al autor de la llamada.

 

 




