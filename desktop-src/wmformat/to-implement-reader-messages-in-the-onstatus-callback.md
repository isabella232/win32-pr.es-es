---
title: Para implementar mensajes de lector en la devolución de llamada de estado
description: Para implementar mensajes de lector en la devolución de llamada de estado
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF), implementar mensajes de lector
- ASF (formato de sistemas avanzados), implementación de mensajes de lector
- Advanced Systems Format (ASF), alstatus callback
- ASF (formato de sistemas avanzados), devolución de llamada en estado
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementar mensajes de lector
- Método de devolución de llamada de estado, implementar mensajes de lector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077304"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="3c3c6-111">Para implementar mensajes de lector en la devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="3c3c6-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="3c3c6-112">Para usar el lector asincrónico para ofrecer contenido desde un archivo ASF, debe implementar un mínimo de dos métodos de devolución de llamada, [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) y [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="3c3c6-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="3c3c6-113">En esta sección se describe cómo implementar **IWMStatusCallback::** en el estado para recibir y responder a los mensajes de estado enviados por el lector.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="3c3c6-114">Los demás objetos del SDK de Windows Media Format usan el **Estado** .</span><span class="sxs-lookup"><span data-stu-id="3c3c6-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="3c3c6-115">Para obtener información general sobre el **Estado**, consulte [usar la devolución de llamada de estado](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="3c3c6-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="3c3c6-116">Al usar el lector asincrónico, debe interceptar los mensajes siguientes en **IWMStatusCallback:: en status**.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="3c3c6-117">Mensaje de estado</span><span class="sxs-lookup"><span data-stu-id="3c3c6-117">Status message</span></span> | <span data-ttu-id="3c3c6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c3c6-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="3c3c6-119">WMT \_ abierto</span><span class="sxs-lookup"><span data-stu-id="3c3c6-119">WMT\_OPENED</span></span>    | <span data-ttu-id="3c3c6-120">Se envía cuando se completan las operaciones de apertura de archivos.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="3c3c6-121">WMT \_ cerrado</span><span class="sxs-lookup"><span data-stu-id="3c3c6-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="3c3c6-122">Se envía cuando se completan las operaciones de cierre de archivos.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="3c3c6-123">Debe usar los mensajes de estado enumerados anteriormente para controlar la ejecución de la aplicación de lectura.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="3c3c6-124">Por ejemplo, debe esperar hasta recibir el mensaje **de \_ Open WMT** para iniciar el lector o llamar a otros métodos que requieran que el lector tenga un archivo listo.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="3c3c6-125">Con frecuencia, las aplicaciones compiladas con el lector asincrónico usan un evento para indicar la finalización de las llamadas asincrónicas y continuar con el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="3c3c6-126">Para obtener más información sobre el uso de eventos para indicar la finalización de las operaciones, vea [uso de eventos con llamadas asincrónicas](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="3c3c6-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="3c3c6-127">El objeto de lectura envía muchos otros mensajes al **Estado** para permitir que la aplicación responda al estado de las operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="3c3c6-128">Los valores posibles de los mensajes de estado se definen en el tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="3c3c6-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c3c6-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c3c6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c3c6-130">**IWMStatusCallback:: en el estado**</span><span class="sxs-lookup"><span data-stu-id="3c3c6-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="3c3c6-131">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="3c3c6-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="3c3c6-132">**Usar la devolución de llamada en estado**</span><span class="sxs-lookup"><span data-stu-id="3c3c6-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




