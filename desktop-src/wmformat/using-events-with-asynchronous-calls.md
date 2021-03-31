---
title: Usar eventos con llamadas asincrónicas
description: Usar eventos con llamadas asincrónicas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- SDK de Windows Media Format, eventos con llamadas asincrónicas
- SDK de Windows Media Format, eventos de llamada asincrónica
- eventos, llamadas asincrónicas
- eventos de llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419028"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="91f91-107">Usar eventos con llamadas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="91f91-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="91f91-108">Con frecuencia, al utilizar métodos a los que se llama de forma asincrónica, querrá detener el procesamiento de la aplicación hasta que el método complete el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="91f91-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="91f91-109">Puede implementar cualquier técnica que desee para controlar esta situación.</span><span class="sxs-lookup"><span data-stu-id="91f91-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="91f91-110">En esta sección se describe el uso de un evento para esperar llamadas asincrónicas en el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="91f91-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="91f91-111">Esta técnica se usa con frecuencia con el SDK de Windows Media Format y se muestra en algunas de las aplicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="91f91-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="91f91-112">En la lista siguiente se resume el uso de eventos para esperar llamadas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="91f91-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="91f91-113">Cree un evento para usarlo con la aplicación mediante una llamada a la función **CreateEvent** del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="91f91-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="91f91-114">Al implementar las devoluciones de llamada adecuadas para la aplicación, Capture los mensajes que debe esperar.</span><span class="sxs-lookup"><span data-stu-id="91f91-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="91f91-115">En la lógica de control de mensajes para los mensajes deseados, señale el evento llamando a la función **SetEvent** del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="91f91-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="91f91-116">Después de que se realicen llamadas a eventos asincrónicos en la aplicación, espere a que el evento señale llamando a la función **WaitForSingleObject** del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="91f91-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="91f91-117">Si diseña una aplicación para Windows, debe crear un bucle para comprobar los mensajes de Windows e incluir una llamada a **WaitForSingleObject** en el bucle con un breve tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="91f91-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91f91-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91f91-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f91-119">**Usar los métodos de devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="91f91-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




