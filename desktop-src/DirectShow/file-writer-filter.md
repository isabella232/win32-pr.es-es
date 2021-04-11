---
description: Filtro de escritor de archivos
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro de escritor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274777"
---
# <a name="file-writer-filter"></a><span data-ttu-id="2d081-103">Filtro de escritor de archivos</span><span class="sxs-lookup"><span data-stu-id="2d081-103">File Writer Filter</span></span>

<span data-ttu-id="2d081-104">El filtro del escritor de archivos se puede usar para escribir archivos en el disco independientemente del formato.</span><span class="sxs-lookup"><span data-stu-id="2d081-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="2d081-105">El filtro simplemente escribe en el disco lo que reciba en su PIN de entrada, por lo que se debe conectar al nivel superior a un multiplexor que pueda dar formato al archivo correctamente.</span><span class="sxs-lookup"><span data-stu-id="2d081-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="2d081-106">Puede crear un nuevo archivo de salida con el escritor de archivos o especificar un archivo existente. Si el archivo ya existe, se sobrescribirá por completo con los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="2d081-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="2d081-107">El filtro del escritor de archivos utiliza las marcas de tiempo del flujo de entrada como desplazamientos de archivo y proporciona acceso aleatorio al archivo.</span><span class="sxs-lookup"><span data-stu-id="2d081-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="2d081-108">Admite **IStream** para permitir la lectura y escritura del encabezado de archivo después de que el gráfico se detenga.</span><span class="sxs-lookup"><span data-stu-id="2d081-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="2d081-109">Para mejorar el rendimiento, también admite escrituras superpuestas no almacenadas en búfer y controla la negociación de búfer correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d081-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="2d081-110">Para escribir archivos ASF, use el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="2d081-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d081-111">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="2d081-111">Filter Interfaces</span></span>                        | <span data-ttu-id="2d081-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="2d081-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="2d081-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="2d081-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="2d081-114">\_Secuencia MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="2d081-114">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="2d081-115">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="2d081-115">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2d081-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="2d081-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="2d081-117">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="2d081-117">Output Pin Media Types</span></span>                   | <span data-ttu-id="2d081-118">No aplicable</span><span class="sxs-lookup"><span data-stu-id="2d081-118">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="2d081-119">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="2d081-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2d081-120">No aplicable</span><span class="sxs-lookup"><span data-stu-id="2d081-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="2d081-121">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="2d081-121">Filter CLSID</span></span>                             | <span data-ttu-id="2d081-122">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="2d081-122">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="2d081-123">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="2d081-123">Property Page CLSID</span></span>                      | <span data-ttu-id="2d081-124">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="2d081-124">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="2d081-125">Executable</span><span class="sxs-lookup"><span data-stu-id="2d081-125">Executable</span></span>                               | <span data-ttu-id="2d081-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="2d081-126">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="2d081-127">Fundament</span><span class="sxs-lookup"><span data-stu-id="2d081-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="2d081-128">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="2d081-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="2d081-129">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="2d081-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2d081-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2d081-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="2d081-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d081-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d081-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d081-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



