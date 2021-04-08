---
title: Objeto de receptor de inserciones de escritor
description: Objeto de receptor de inserciones de escritor
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- SDK de Windows Media Format, objetos de receptor de extracción de escritor
- Advanced Systems Format (ASF), objetos de receptor de inserciones de escritor
- ASF (formato de sistemas avanzados), objetos de receptor de inserciones de escritor
- objetos, objetos de receptor de inserciones de escritor
- objetos de receptor de inserciones de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994939"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="8c436-108">Objeto de receptor de inserciones de escritor</span><span class="sxs-lookup"><span data-stu-id="8c436-108">Writer Push Sink Object</span></span>

<span data-ttu-id="8c436-109">El objeto de receptor de inserciones del escritor distribuye los medios digitales a los puntos de publicación.</span><span class="sxs-lookup"><span data-stu-id="8c436-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="8c436-110">Por ejemplo, un concierto en directo se puede codificar mediante un solo servidor y, a continuación, entregarse o *insertarse* en otros servidores que realmente transmitirán el contenido a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8c436-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="8c436-111">La función [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)crea un objeto de receptor de inserciones de escritor, que establece un puntero a una interfaz **IWMWriterPushSink** .</span><span class="sxs-lookup"><span data-stu-id="8c436-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="8c436-112">Las demás interfaces admitidas por el objeto, que se enumeran en la tabla siguiente, se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8c436-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="8c436-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="8c436-113">Interface</span></span>                                          | <span data-ttu-id="8c436-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c436-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c436-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="8c436-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="8c436-116">Permite que la aplicación obtenga mensajes de estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c436-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="8c436-117">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="8c436-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="8c436-118">Administra una sesión de distribución de la extracción.</span><span class="sxs-lookup"><span data-stu-id="8c436-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="8c436-119">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="8c436-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="8c436-120">Asigna memoria, determina si el receptor está funcionando en tiempo real y expone varias funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8c436-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="8c436-121">La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor de inserciones del escritor.</span><span class="sxs-lookup"><span data-stu-id="8c436-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="8c436-122">Interfaz</span><span class="sxs-lookup"><span data-stu-id="8c436-122">Interface</span></span>                                      | <span data-ttu-id="8c436-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c436-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="8c436-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="8c436-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="8c436-125">Obligatorio cuando la información de estado se debe comunicar a la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="8c436-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c436-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c436-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c436-127">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="8c436-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="8c436-128">**Envío de datos ASF a un punto de publicación**</span><span class="sxs-lookup"><span data-stu-id="8c436-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="8c436-129">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="8c436-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




