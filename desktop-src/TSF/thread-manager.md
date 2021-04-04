---
title: Administrador de subprocesos
description: El administrador de subprocesos es el componente base del administrador de TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Marco de trabajo de servicios de texto (TSF), administrador de subprocesos
- TSF (marco de trabajo de servicios de texto), administrador de subprocesos
- servicios de texto, administrador de subprocesos
- Aplicaciones habilitadas para TSF, administrador de subprocesos
- Administrador de subprocesos
- Administrador de TSF
- notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077999"
---
# <a name="thread-manager"></a><span data-ttu-id="edd19-110">Administrador de subprocesos</span><span class="sxs-lookup"><span data-stu-id="edd19-110">Thread Manager</span></span>

<span data-ttu-id="edd19-111">El administrador de subprocesos es el componente base del administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="edd19-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="edd19-112">El administrador de subprocesos realiza tareas comunes relacionadas con aplicaciones y servicios de texto (clientes).</span><span class="sxs-lookup"><span data-stu-id="edd19-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="edd19-113">Estas tareas incluyen, entre otras, la activación y desactivación de los servicios de texto TSF, la creación de administradores de documentos y el mantenimiento de la relación adecuada entre documentos y el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="edd19-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="edd19-114">El administrador de subprocesos se define mediante la interfaz [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .</span><span class="sxs-lookup"><span data-stu-id="edd19-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="edd19-115">La mayoría de las interfaces y los objetos proporcionados por el administrador de TSF se pueden obtener utilizando los métodos proporcionados por la interfaz del administrador de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="edd19-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="edd19-116">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="edd19-116">Applications</span></span>

<span data-ttu-id="edd19-117">Una aplicación crea un objeto administrador de subprocesos llamando a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ TFThreadMgr.</span><span class="sxs-lookup"><span data-stu-id="edd19-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="edd19-118">Servicios de texto</span><span class="sxs-lookup"><span data-stu-id="edd19-118">Text Services</span></span>

<span data-ttu-id="edd19-119">Un servicio de texto obtiene un objeto de administrador de subprocesos en el método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="edd19-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="edd19-120">Notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="edd19-120">Event Notifications</span></span>

<span data-ttu-id="edd19-121">El administrador de subprocesos también proporciona la notificación de eventos a los clientes.</span><span class="sxs-lookup"><span data-stu-id="edd19-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="edd19-122">En TSF, las notificaciones de eventos se proporcionan por medio de un receptor de eventos, que es un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="edd19-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="edd19-123">Para recibir notificaciones del administrador de subprocesos, un cliente implementa un objeto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e instala el receptor de eventos.</span><span class="sxs-lookup"><span data-stu-id="edd19-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="edd19-124">El receptor de eventos se instala consultando el administrador de subprocesos para IID \_ ITfSource y llamando a [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfThreadMgrEventSink.</span><span class="sxs-lookup"><span data-stu-id="edd19-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edd19-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edd19-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd19-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="edd19-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="edd19-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="edd19-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="edd19-128">ITfTextInputProcessor:: Activate</span><span class="sxs-lookup"><span data-stu-id="edd19-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="edd19-129">ITfThreadMgrEventSink</span><span class="sxs-lookup"><span data-stu-id="edd19-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="edd19-130">ITfSource::AdviseSink</span><span class="sxs-lookup"><span data-stu-id="edd19-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 