---
title: Usar receptores personalizados
description: Usar receptores personalizados
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF), receptores personalizados
- ASF (formato de sistemas avanzados), receptores personalizados
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores personalizados
- receptores personalizados, acerca de
- receptores de escritor, receptores personalizados
- receptores personalizados, interfaz IWMWriterSink
- IWMWriterSink
- receptores de escritor, interfaz IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788751"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="19dd8-113">Usar receptores personalizados</span><span class="sxs-lookup"><span data-stu-id="19dd8-113">Using Custom Sinks</span></span>

<span data-ttu-id="19dd8-114">Si tiene una necesidad especial de escritura, puede crear sus propios receptores de escritor.</span><span class="sxs-lookup"><span data-stu-id="19dd8-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="19dd8-115">El sistema de escritura mantiene la comunicación unidireccional con un receptor realizando llamadas a los métodos de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span><span class="sxs-lookup"><span data-stu-id="19dd8-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="19dd8-116">Para crear su propio receptor, implemente la interfaz **IWMWriterSink** en una clase de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19dd8-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="19dd8-117">Este proceso es muy similar a la implementación de cualquier otra interfaz de devolución de llamada utilizada por los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="19dd8-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="19dd8-118">Para obtener más información sobre las devoluciones de llamada, vea [usar los métodos de devolución de llamada](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="19dd8-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="19dd8-119">El búfer recibido en [**IWMWriterSink:: MyHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) debe escribirse en el principio del archivo y todos los búferes recibidos en [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) se deben escribir secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="19dd8-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="19dd8-120">Se llama al método **MyHeader** al principio, pero también se le puede llamar en otros momentos, y si es así, debe sobrescribir el encabezado original, si es posible.</span><span class="sxs-lookup"><span data-stu-id="19dd8-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="19dd8-121">Si, por algún motivo, la aplicación no puede realizar esta tarea, simplemente omita las llamadas de un **subcabezal** posteriores.</span><span class="sxs-lookup"><span data-stu-id="19dd8-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="19dd8-122">El receptor personalizado debe comunicar su estado a la aplicación de escritura realizando llamadas al método de devolución de llamada [**IWMStatusCallback:: Alstatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="19dd8-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="19dd8-123">Si implementa el receptor como un objeto COM, es posible que desee exponer la interfaz [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="19dd8-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="19dd8-124">Sin embargo, puede pasar la dirección de la devolución de llamada de **Estado** al receptor y establecer un contexto de la forma que desee.</span><span class="sxs-lookup"><span data-stu-id="19dd8-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19dd8-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19dd8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19dd8-126">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="19dd8-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




