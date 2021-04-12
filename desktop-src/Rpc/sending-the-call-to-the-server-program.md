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
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="24263-104">Enviar la llamada al programa de servidor</span><span class="sxs-lookup"><span data-stu-id="24263-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="24263-105">Una vez que el tiempo de ejecución de RPC del cliente se ha conectado al punto de conexión del servidor, calcula las referencias de los argumentos y los envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="24263-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="24263-106">El tiempo de ejecución de RPC del servidor proporciona al código auxiliar los argumentos de cálculo de referencias que los elimina y, a continuación, los pasa a las rutinas de servidor.</span><span class="sxs-lookup"><span data-stu-id="24263-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="24263-107">Cuando se devuelven las rutinas de servidor, el código auxiliar recoge los \[ \] parámetros out y \[ in, out \] y el valor devuelto, los calcula de las referencias y envía los datos de cálculo de referencias al tiempo de ejecución de RPC del servidor.</span><span class="sxs-lookup"><span data-stu-id="24263-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="24263-108">El tiempo de ejecución de RPC envía los datos de vuelta al cliente, donde el tiempo de ejecución de RPC del cliente los entrega al código auxiliar del lado cliente que los quita y los devuelve al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="24263-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




