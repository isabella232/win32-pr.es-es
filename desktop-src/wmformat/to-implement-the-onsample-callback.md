---
title: Para implementar la devolución de llamada de ejemplo
description: Para implementar la devolución de llamada de ejemplo
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), implementación de la devolución de llamada en estado
- ASF (formato de sistemas avanzados), implementación de la devolución de llamada en estado
- Advanced Systems Format (ASF), alstatus callback
- ASF (formato de sistemas avanzados), devolución de llamada en estado
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementar la devolución de llamada en estado
- Método de devolución de llamada en estado, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358766"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="0d09b-111">Para implementar la devolución de llamada de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d09b-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="0d09b-112">El lector asincrónico proporciona ejemplos a la aplicación de control en el orden en tiempo de presentación realizando llamadas al método de devolución de llamada [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) MyMethod.</span><span class="sxs-lookup"><span data-stu-id="0d09b-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="0d09b-113">Al crear una aplicación mediante el lector asincrónico, debe implementar el **ejemplo** para tratar con ejemplos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="0d09b-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="0d09b-114">Normalmente, las funciones o los métodos creados para representar el contenido se llamarán desde en el **ejemplo**.</span><span class="sxs-lookup"><span data-stu-id="0d09b-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="0d09b-115">La implementación típica de la devolución de llamada de **ejemplo** incluye los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0d09b-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="0d09b-116">Recupere la ubicación y el tamaño del búfer que contiene el ejemplo llamando a [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) en el búfer pasado como *pSample*.</span><span class="sxs-lookup"><span data-stu-id="0d09b-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="0d09b-117">Bifurcar la lógica según el número de salida.</span><span class="sxs-lookup"><span data-stu-id="0d09b-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="0d09b-118">El número de salida se pasa a la **muestra** como *dwOutputNumber*.</span><span class="sxs-lookup"><span data-stu-id="0d09b-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="0d09b-119">Incluya la lógica de representación para cada número de salida que desee admitir.</span><span class="sxs-lookup"><span data-stu-id="0d09b-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="0d09b-120">Si está representando ejemplos de varias salidas, puede que necesite sincronizar la representación.</span><span class="sxs-lookup"><span data-stu-id="0d09b-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="0d09b-121">Las aplicaciones que proporcionan ejemplos comprimidos de archivos ASF deben implementar el método de devolución de llamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="0d09b-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="0d09b-122">**OnStreamSample** funciona de forma casi idéntica al **ejemplo**, salvo que recibe muestras comprimidas por número de secuencia en lugar de muestras sin comprimir por número de salida.</span><span class="sxs-lookup"><span data-stu-id="0d09b-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d09b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d09b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d09b-124">**Interfaz IWMReaderCallback**</span><span class="sxs-lookup"><span data-stu-id="0d09b-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="0d09b-125">**Interfaz IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="0d09b-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="0d09b-126">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="0d09b-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="0d09b-127">**Usar los métodos de devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="0d09b-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




