---
description: Errores de componentes en cola
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Errores de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714853"
---
# <a name="queued-components-errors"></a><span data-ttu-id="37594-103">Errores de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="37594-103">Queued Components Errors</span></span>

<span data-ttu-id="37594-104">Cuando se produce un error en una llamada a un componente en cola, ya sea porque no se pudo transmitir al servidor (un error del lado cliente) o porque no se pudo ejecutar cuando llegó (un error del servidor), el mensaje de [Message Queue](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Server correspondiente recibe el nombre de mensaje *dudoso*.</span><span class="sxs-lookup"><span data-stu-id="37594-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="37594-105">El servicio de componentes en cola de COM+ controla los mensajes dudosos mediante una serie de colas de reintento.</span><span class="sxs-lookup"><span data-stu-id="37594-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="37594-106">Después de varios reintentos, el mensaje se mueve a una cola de finalización.</span><span class="sxs-lookup"><span data-stu-id="37594-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="37594-107">Los mensajes permanecen en la cola de permanencia hasta que se mueven manualmente mediante la utilidad del Movedor de mensajes de componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="37594-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="37594-108">Para obtener más información acerca del uso del Movedor de mensajes, consulte [control de errores](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="37594-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="37594-109">Puede encontrar descripciones detalladas de la secuencia de eventos que se produce para diversos tipos de errores en los temas que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="37594-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="37594-110">Tema</span><span class="sxs-lookup"><span data-stu-id="37594-110">Topic</span></span>                                                                             | <span data-ttu-id="37594-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37594-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37594-112">Errores del lado servidor</span><span class="sxs-lookup"><span data-stu-id="37594-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="37594-113">Describe en detalle la respuesta del servicio de componentes en cola de COM+ a un error del servidor.</span><span class="sxs-lookup"><span data-stu-id="37594-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="37594-114">Errores del lado cliente</span><span class="sxs-lookup"><span data-stu-id="37594-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="37594-115">Describe en detalle la respuesta del servicio de componentes en cola de COM+ a un error del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="37594-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="37594-116">Errores de Client-Side persistentes</span><span class="sxs-lookup"><span data-stu-id="37594-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="37594-117">Describe en detalle la respuesta del servicio de componentes en cola de COM+ a errores repetidos del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="37594-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




