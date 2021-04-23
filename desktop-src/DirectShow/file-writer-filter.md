---
description: Filtro del escritor de archivos
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro del escritor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909693"
---
# <a name="file-writer-filter"></a><span data-ttu-id="b9eda-103">Filtro del escritor de archivos</span><span class="sxs-lookup"><span data-stu-id="b9eda-103">File Writer Filter</span></span>

<span data-ttu-id="b9eda-104">El filtro Escritor de archivos se puede usar para escribir archivos en el disco independientemente del formato.</span><span class="sxs-lookup"><span data-stu-id="b9eda-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="b9eda-105">El filtro simplemente escribe en el disco lo que recibe en su pin de entrada, por lo que debe estar conectado ascendentemente a un multiplexor que pueda dar formato al archivo correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9eda-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="b9eda-106">Puede crear un nuevo archivo de salida con el escritor de archivos o especificar un archivo existente. Si el archivo ya existe, se sobrescribirá completamente con los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="b9eda-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="b9eda-107">El filtro de escritor de archivos usa las marcas de tiempo del flujo de entrada como desplazamientos de archivo y proporciona acceso aleatorio al archivo.</span><span class="sxs-lookup"><span data-stu-id="b9eda-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="b9eda-108">Admite **IStream para** permitir la lectura y escritura del encabezado de archivo después de detener el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b9eda-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="b9eda-109">Para mejorar el rendimiento, también admite escrituras superpuestas no almacenadas en búfer y controla la negociación de búfer correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b9eda-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="b9eda-110">Para escribir archivos ASF, use el filtro [WM ASF Writer.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="b9eda-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="b9eda-111">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b9eda-111">Label</span></span> | <span data-ttu-id="b9eda-112">Value</span><span class="sxs-lookup"><span data-stu-id="b9eda-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eda-113">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="b9eda-113">Filter Interfaces</span></span>                        | <span data-ttu-id="b9eda-114">[**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b9eda-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="b9eda-115">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="b9eda-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="b9eda-116">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="b9eda-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="b9eda-117">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="b9eda-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b9eda-118">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**</span><span class="sxs-lookup"><span data-stu-id="b9eda-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="b9eda-119">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="b9eda-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="b9eda-120">No aplicable</span><span class="sxs-lookup"><span data-stu-id="b9eda-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="b9eda-121">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="b9eda-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b9eda-122">No aplicable</span><span class="sxs-lookup"><span data-stu-id="b9eda-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="b9eda-123">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="b9eda-123">Filter CLSID</span></span>                             | <span data-ttu-id="b9eda-124">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="b9eda-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="b9eda-125">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b9eda-125">Property Page CLSID</span></span>                      | <span data-ttu-id="b9eda-126">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b9eda-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b9eda-127">Executable</span><span class="sxs-lookup"><span data-stu-id="b9eda-127">Executable</span></span>                               | <span data-ttu-id="b9eda-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="b9eda-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="b9eda-129">Mérito</span><span class="sxs-lookup"><span data-stu-id="b9eda-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="b9eda-130">NO USE EL VALOR DE NO \_ \_ \_ USE.</span><span class="sxs-lookup"><span data-stu-id="b9eda-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="b9eda-131">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="b9eda-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b9eda-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b9eda-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b9eda-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9eda-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9eda-134">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b9eda-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



