---
title: Funciones de devolución de llamada de estado
description: Funciones de devolución de llamada de estado
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funciones de devolución de llamada AVICap, estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418702"
---
# <a name="status-callback-functions"></a><span data-ttu-id="f4abd-104">Funciones de devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="f4abd-104">Status Callback Functions</span></span>

<span data-ttu-id="f4abd-105">Una ventana de captura puede enviar mensajes a la función de devolución de llamada de estado durante la captura de vídeo en disco o durante otras operaciones largas para notificar a la aplicación el progreso de una operación.</span><span class="sxs-lookup"><span data-stu-id="f4abd-105">A capture window can send messages to the status callback function while capturing video to disk or during other lengthy operations to notify your application of the progress of an operation.</span></span> <span data-ttu-id="f4abd-106">La información de estado incluye un identificador de mensaje y una cadena de texto con formato lista para su presentación.</span><span class="sxs-lookup"><span data-stu-id="f4abd-106">The status information includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="f4abd-107">La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se van a presentar al usuario.</span><span class="sxs-lookup"><span data-stu-id="f4abd-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="f4abd-108">Durante las operaciones de captura, el primer mensaje enviado a la función de devolución de llamada es siempre ID \_ Cap \_ Begin y el último es el extremo de los identificadores \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f4abd-108">During capture operations, the first message sent to the callback function is always IDS\_CAP\_BEGIN and the last is always IDS\_CAP\_END.</span></span> <span data-ttu-id="f4abd-109">Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="f4abd-109">A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.</span></span>

 

 




