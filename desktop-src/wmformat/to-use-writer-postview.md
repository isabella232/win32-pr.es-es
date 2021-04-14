---
title: Para usar la vista previa del escritor
description: Para usar la vista previa del escritor
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), postview del escritor
- ASF (formato de sistemas avanzados), postview del escritor
- Advanced Systems Format (ASF), postview
- ASF (formato de sistemas avanzados), postview
- vista previa del escritor
- vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533052"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="24dae-109">Para usar la vista previa del escritor</span><span class="sxs-lookup"><span data-stu-id="24dae-109">To Use Writer Postview</span></span>

<span data-ttu-id="24dae-110">El objeto escritor proporciona funciones de postview para que pueda comprobar el contenido escrito sin tener que configurar el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="24dae-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="24dae-111">El objeto de escritor no admite la postview para el contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="24dae-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="24dae-112">El postvisor del escritor funciona de manera muy similar al objeto lector asincrónico, solo con menos características.</span><span class="sxs-lookup"><span data-stu-id="24dae-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="24dae-113">Para obtener información detallada sobre cómo leer archivos multimedia digitales, consulte [lectura de archivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="24dae-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="24dae-114">Para implementar el postvisor, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="24dae-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="24dae-115">Implemente la devolución de llamada [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="24dae-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="24dae-116">Este método es esencialmente el mismo que [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , salvo que especifica los números de secuencia en lugar de los resultados.</span><span class="sxs-lookup"><span data-stu-id="24dae-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="24dae-117">Configure para escritura como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="24dae-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="24dae-118">Obtenga un puntero a la interfaz [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) del objeto de escritor llamando a **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="24dae-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="24dae-119">Establezca la devolución de llamada para que la use el postvisor mediante una llamada a [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span><span class="sxs-lookup"><span data-stu-id="24dae-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="24dae-120">Para cada secuencia para la que desea recibir ejemplos de postview, llame a [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="24dae-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="24dae-121">Puede comprobar si un flujo está configurado para recibir ejemplos de postview mediante una llamada a [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="24dae-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="24dae-122">Puede manipular los formatos de ejemplo, del mismo modo que lo haría con los formatos de salida del objeto lector o del objeto lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="24dae-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="24dae-123">Cuando empiece a escribir el archivo, comenzará a recibir ejemplos en su implementación del método de devolución de llamada **OnPostViewSample** .</span><span class="sxs-lookup"><span data-stu-id="24dae-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24dae-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24dae-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24dae-125">**Interfaz IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="24dae-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="24dae-126">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="24dae-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




