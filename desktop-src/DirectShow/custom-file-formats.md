---
description: Formatos de archivo personalizados
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Formatos de archivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361dca97fcd34b30e3c29d6ba189ad26968d4fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997867"
---
# <a name="custom-file-formats"></a><span data-ttu-id="6df8b-103">Formatos de archivo personalizados</span><span class="sxs-lookup"><span data-stu-id="6df8b-103">Custom File Formats</span></span>

<span data-ttu-id="6df8b-104">Si tiene un filtro personalizado MUX o de escritor de archivos que admite su propio formato de archivo, puede especificar el CLSID como el primer parámetro del método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="6df8b-104">If you have a custom mux or file-writer filter that supports your own file format, you can specify the CLSID as the first parameter of the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



<span data-ttu-id="6df8b-105">Para obtener más información sobre este uso, vea [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="6df8b-105">For more information about this usage, see [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df8b-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6df8b-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df8b-107">Capturar vídeo en un archivo</span><span class="sxs-lookup"><span data-stu-id="6df8b-107">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



