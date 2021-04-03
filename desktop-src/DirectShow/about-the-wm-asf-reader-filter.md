---
description: Acerca del filtro de lector ASF de WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Acerca del filtro de lector ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906773"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="269e2-103">Acerca del filtro de lector ASF de WM</span><span class="sxs-lookup"><span data-stu-id="269e2-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="269e2-104">La reproducción de archivos ASF se controla mediante el filtro [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="269e2-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="269e2-105">Cuando el lector ASF de WM lee un archivo, crea automáticamente un PIN de salida para cada flujo, incluidas las secuencias Web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria.</span><span class="sxs-lookup"><span data-stu-id="269e2-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="269e2-106">En el caso de varios archivos de velocidad de bits, los pin solo se crean para las secuencias seleccionadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="269e2-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="269e2-107">Para reproducir un archivo ASF con el filtro de lector ASF de WM, llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="269e2-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="269e2-108">El lector ASF de WM admite la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de DirectShow, que permite a las aplicaciones realizar búsquedas temporales en el archivo.</span><span class="sxs-lookup"><span data-stu-id="269e2-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="269e2-109">Sin embargo, no se admite la reproducción a velocidades distintas de 1,0 (tal y como se especifica en [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)).</span><span class="sxs-lookup"><span data-stu-id="269e2-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="269e2-110">El filtro lector ASF de WM también expone varias interfaces del SDK de Windows Media Format, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="269e2-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="269e2-111">Estas interfaces se documentan en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="269e2-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="269e2-112">Interfaz</span><span class="sxs-lookup"><span data-stu-id="269e2-112">Interface</span></span>                                             | <span data-ttu-id="269e2-113">Cómo se exponen</span><span class="sxs-lookup"><span data-stu-id="269e2-113">How exposed</span></span>                                 | <span data-ttu-id="269e2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="269e2-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e2-115">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="269e2-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="269e2-116">A través de **IServiceProvider** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="269e2-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="269e2-117">Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Rights Management digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="269e2-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="269e2-118">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="269e2-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="269e2-119">**QueryInterface** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="269e2-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="269e2-120">Proporcionado para que las aplicaciones puedan leer atributos de archivo y de contenido, así como información de marcadores y metadatos.</span><span class="sxs-lookup"><span data-stu-id="269e2-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="269e2-121">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="269e2-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="269e2-122">**QueryInterface** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="269e2-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="269e2-123">Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector de WM.</span><span class="sxs-lookup"><span data-stu-id="269e2-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="269e2-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="269e2-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="269e2-125">**QueryInterface** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="269e2-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="269e2-126">Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector SDK Reader.</span><span class="sxs-lookup"><span data-stu-id="269e2-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="269e2-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="269e2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269e2-128">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="269e2-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



