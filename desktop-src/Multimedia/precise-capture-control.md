---
title: Control de captura preciso
description: Control de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funciones de devolución de llamada AVICap, control de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532085"
---
# <a name="precise-capture-control"></a><span data-ttu-id="6865a-104">Control de captura preciso</span><span class="sxs-lookup"><span data-stu-id="6865a-104">Precise Capture Control</span></span>

<span data-ttu-id="6865a-105">Una ventana de captura puede proporcionar la función de devolución de llamada del control de captura con un control preciso sobre los momentos en que comienza y finaliza la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="6865a-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="6865a-106">El primer mensaje enviado desde el controlador de captura al procedimiento de devolución de llamada establece el parámetro *nState* en CONTROLCALLBACK \_ preroll después de asignar todos los búferes y se completan todos los demás preparados de captura.</span><span class="sxs-lookup"><span data-stu-id="6865a-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="6865a-107">Este mensaje ofrece a la aplicación la posibilidad de revertir los orígenes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6865a-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="6865a-108">(La función de devolución de llamada especifica *nState* como el segundo parámetro). A continuación, la función de devolución de llamada devuelve en el momento en que se inicia la grabación exacta.</span><span class="sxs-lookup"><span data-stu-id="6865a-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="6865a-109">Un valor devuelto de **true** desde la función de devolución de llamada continúa la captura.</span><span class="sxs-lookup"><span data-stu-id="6865a-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="6865a-110">Un valor devuelto de **false** anula la captura.</span><span class="sxs-lookup"><span data-stu-id="6865a-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="6865a-111">Una vez que se inicia la captura, se llama a la función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK \_ para permitir que la aplicación finalice la captura devolviendo **false**.</span><span class="sxs-lookup"><span data-stu-id="6865a-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




