---
title: Para recuperar ejemplos de medios con el lector sincrónico
description: Para recuperar ejemplos de medios con el lector sincrónico
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de medios
- ASF (formato de sistemas avanzados), recuperar ejemplos de medios
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, recuperar ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420268"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="97c43-108">Para recuperar ejemplos de medios con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="97c43-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="97c43-109">Debe solicitar cada ejemplo de uno en uno desde el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="97c43-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="97c43-110">Esto le proporciona más control sobre los ejemplos que recibe y cuándo los recibe.</span><span class="sxs-lookup"><span data-stu-id="97c43-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="97c43-111">Use el método [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="97c43-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="97c43-112">Debe pasar principalmente punteros a variables que se rellenarán con información sobre el ejemplo recuperado como parámetros.</span><span class="sxs-lookup"><span data-stu-id="97c43-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="97c43-113">El único parámetro de entrada es *wStreamNum*.</span><span class="sxs-lookup"><span data-stu-id="97c43-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="97c43-114">Si pasa un número de secuencia, **GetNextSample** recuperará el siguiente ejemplo con el número de secuencia especificado.</span><span class="sxs-lookup"><span data-stu-id="97c43-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="97c43-115">Si pasa cero para *wStreamNum*, se recupera el siguiente ejemplo que se produce cronológicamente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="97c43-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="97c43-116">De forma predeterminada, el lector sincrónico recupera todos los ejemplos de las salidas de un archivo en orden cronológico.</span><span class="sxs-lookup"><span data-stu-id="97c43-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="97c43-117">Si llama a **GetNextSample** y no hay más ejemplos para obtener, devolverá NS \_ E \_ ningún \_ ejemplo más \_ , que es un código de error erróneo.</span><span class="sxs-lookup"><span data-stu-id="97c43-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="97c43-118">Al codificar por lo tanto, simplemente puede recorrer los ejemplos hasta que se produzca un error en el método.</span><span class="sxs-lookup"><span data-stu-id="97c43-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="97c43-119">Para asegurarse de que el lector sincrónico ofrezca duraciones de ejemplo correctas para las secuencias de vídeo, primero debe configurar la salida de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="97c43-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="97c43-120">Llame al método [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para establecer el valor de g \_ wszVideoSampleDurations en **true**.</span><span class="sxs-lookup"><span data-stu-id="97c43-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="97c43-121">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="97c43-121">Example Code</span></span>

<span data-ttu-id="97c43-122">En el ejemplo de código siguiente se muestra cómo usar **GetNextSample** para recuperar todos los ejemplos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="97c43-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="97c43-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97c43-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97c43-124">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="97c43-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="97c43-125">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="97c43-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




