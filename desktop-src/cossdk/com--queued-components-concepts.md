---
description: Conceptos de componentes en cola de COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Conceptos de componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705277"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="1f761-103">Conceptos de componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="1f761-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="1f761-104">En función de los servicios de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , el servicio de componentes en cola de com+ proporciona una manera sencilla de invocar y ejecutar componentes de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1f761-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="1f761-105">El procesamiento se puede realizar sin tener en cuenta la disponibilidad o la accesibilidad del remitente o del receptor.</span><span class="sxs-lookup"><span data-stu-id="1f761-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="1f761-106">En términos COM, una *cola* es un área de almacenamiento que guarda los mensajes para su posterior recuperación.</span><span class="sxs-lookup"><span data-stu-id="1f761-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="1f761-107">Queue Server proporciona un mecanismo para la comunicación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1f761-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="1f761-108">Es decir, el remitente y el receptor no se conectan directamente y solo se comunican a través de las colas.</span><span class="sxs-lookup"><span data-stu-id="1f761-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="1f761-109">Queue Server proporciona una manera de conservar la información hasta que el receptor esté listo para obtenerla.</span><span class="sxs-lookup"><span data-stu-id="1f761-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="1f761-110">El remitente y el receptor se comunican indirectamente para que cada uno de ellos pueda funcionar de manera independiente, no se ve afectado por el otro.</span><span class="sxs-lookup"><span data-stu-id="1f761-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="1f761-111">En el pasado, era necesario un conocimiento exhaustivo de la serialización para poner en cola, enviar y recibir mensajes asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="1f761-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="1f761-112">Ahora, el servicio de componentes en cola COM+ calcula automáticamente las referencias a los datos en forma de mensaje de Message Queue Server y los utiliza para los desarrolladores de componentes.</span><span class="sxs-lookup"><span data-stu-id="1f761-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="1f761-113">Y dado que el servicio de componentes en cola ofrece compatibilidad integrada para transacciones, un estado incoherente no puede poner en peligro los datos si se produce un error en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1f761-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="1f761-114">Los temas siguientes de esta sección contienen información general sobre el diseño y la escritura de componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="1f761-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="1f761-115">Tema</span><span class="sxs-lookup"><span data-stu-id="1f761-115">Topic</span></span>                                                                           | <span data-ttu-id="1f761-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f761-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f761-117">Ventajas del procesamiento en cola</span><span class="sxs-lookup"><span data-stu-id="1f761-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="1f761-118">Describe las ventajas de la programación con componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="1f761-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="1f761-119">Arquitectura de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="1f761-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="1f761-120">Describe la arquitectura del servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="1f761-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="1f761-121">Message Queue Server transaccional</span><span class="sxs-lookup"><span data-stu-id="1f761-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="1f761-122">Describe cómo administra las transacciones el servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="1f761-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="1f761-123">Seguridad de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="1f761-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="1f761-124">Describe las opciones de directiva para la autenticación de mensajes de cliente y sus implicaciones.</span><span class="sxs-lookup"><span data-stu-id="1f761-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="1f761-125">Desarrollar componentes en cola</span><span class="sxs-lookup"><span data-stu-id="1f761-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="1f761-126">Describe las consideraciones de programación al escribir componentes de queuable.</span><span class="sxs-lookup"><span data-stu-id="1f761-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="1f761-127">Errores de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="1f761-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="1f761-128">Describe los tipos de errores más comunes que pueden producirse al usar el servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="1f761-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1f761-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f761-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f761-130">Tareas de componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="1f761-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




