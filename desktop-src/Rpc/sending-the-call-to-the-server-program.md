---
title: Envío de la llamada al programa de servidor
description: Una vez que el tiempo de ejecución de RPC del lado cliente se ha conectado al punto de conexión del servidor, se programan los argumentos y se envían al servidor.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Remote Procedure Call RPC , tasks, sending the call to the server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473542"
---
# <a name="sending-the-call-to-the-server-program"></a>Envío de la llamada al programa de servidor

Una vez que el tiempo de ejecución de RPC del lado cliente se ha conectado al punto de conexión del servidor, se programan los argumentos y se envían al servidor. El tiempo de ejecución de RPC del servidor proporciona los argumentos de cifrado al código auxiliar que los desmarca y, a continuación, los pasa a las rutinas del servidor. Cuando se devuelven las rutinas de servidor, el código auxiliar recoge los parámetros out e in,out y el valor devuelto, los programa y envía los datos de salida al tiempo de ejecución rpc del \[ \] \[ \] servidor. El tiempo de ejecución de RPC devuelve los datos al cliente, donde el tiempo de ejecución de RPC del cliente los entrega al código auxiliar del lado cliente que los desmarshalls y los devuelve al autor de la llamada.

 

 




