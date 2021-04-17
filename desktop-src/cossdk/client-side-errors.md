---
description: Errores de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Errores de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705279"
---
# <a name="client-side-errors"></a><span data-ttu-id="0ad67-103">Errores de Client-Side</span><span class="sxs-lookup"><span data-stu-id="0ad67-103">Client-Side Errors</span></span>

<span data-ttu-id="0ad67-104">Los errores del lado cliente se controlan de forma similar a los errores del servidor.</span><span class="sxs-lookup"><span data-stu-id="0ad67-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="0ad67-105">[Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) puede trasladar un mensaje a su cola de destino si, por ejemplo, el mensaje no se puede trasladar del cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="0ad67-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="0ad67-106">En este caso, el mensaje se mueve a la cola de mensajes no enviados del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="0ad67-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="0ad67-107">El servicio de componentes en cola de COM+ supervisa la cola de mensajes con problemas de entrega.</span><span class="sxs-lookup"><span data-stu-id="0ad67-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="0ad67-108">Si se han migrado los mensajes, el servicio de componentes en cola crea una instancia de la clase de excepción y llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span><span class="sxs-lookup"><span data-stu-id="0ad67-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="0ad67-109">Si esto se realiza correctamente, el monitor de cola de mensajes con problemas de entrega invoca [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span><span class="sxs-lookup"><span data-stu-id="0ad67-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="0ad67-110">El objeto puede realizar alguna acción para invertir el efecto de una transacción anterior.</span><span class="sxs-lookup"><span data-stu-id="0ad67-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="0ad67-111">Si se confirma la reproducción, el mensaje se quita de la cola de mensajes con problemas de entrega Xact.</span><span class="sxs-lookup"><span data-stu-id="0ad67-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="0ad67-112">Si se produce un error en la reproducción o el CLSID y la interfaz necesarios no están disponibles, el mensaje permanece en la cola de mensajes con problemas de entrega Xact.</span><span class="sxs-lookup"><span data-stu-id="0ad67-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="0ad67-113">Si necesita intervenir en el proceso descrito anteriormente, o si necesita mover un mensaje dudoso fuera de la cola de salida final, use la utilidad del Movedor de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0ad67-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="0ad67-114">Para obtener más información sobre la utilidad del Movedor de mensajes, vea [control de errores](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="0ad67-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ad67-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ad67-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad67-116">Errores de Client-Side persistentes</span><span class="sxs-lookup"><span data-stu-id="0ad67-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="0ad67-117">Errores del lado servidor</span><span class="sxs-lookup"><span data-stu-id="0ad67-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
