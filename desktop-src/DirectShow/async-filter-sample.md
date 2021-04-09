---
description: Ejemplo de filtro Async
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Ejemplo de filtro Async
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080056"
---
# <a name="async-filter-sample"></a><span data-ttu-id="980f6-103">Ejemplo de filtro Async</span><span class="sxs-lookup"><span data-stu-id="980f6-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="980f6-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="980f6-104">Description</span></span>

<span data-ttu-id="980f6-105">El ejemplo de filtro Async es un filtro de lector de archivos que admite la descarga progresiva.</span><span class="sxs-lookup"><span data-stu-id="980f6-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="980f6-106">Este filtro de ejemplo implementa las interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="980f6-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="980f6-107">Admite archivos MPEG, pero no archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="980f6-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="980f6-108">Uso</span><span class="sxs-lookup"><span data-stu-id="980f6-108">Usage</span></span>

<span data-ttu-id="980f6-109">En este ejemplo se incluye una pequeña aplicación de línea de comandos, Memfile.exe, que muestra el filtro.</span><span class="sxs-lookup"><span data-stu-id="980f6-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="980f6-110">Los argumentos de la línea de comandos especifican un archivo multimedia y una velocidad de bits, en kilobytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="980f6-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="980f6-111">La aplicación lee el archivo en la memoria a la velocidad especificada y reproduce el archivo.</span><span class="sxs-lookup"><span data-stu-id="980f6-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="980f6-112">Para ello, crea una instancia del filtro, agrega el filtro al gráfico de filtro y representa el PIN de salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="980f6-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="980f6-113">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="980f6-113">At the command line, type:</span></span>

<span data-ttu-id="980f6-114">**Velocidad de bits de Memfile FILENAME**</span><span class="sxs-lookup"><span data-stu-id="980f6-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="980f6-115">El filtro de ejemplo Async no admite archivos AVI porque no se puede conectar al filtro de [divisor de AVI](avi-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="980f6-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="980f6-116">El PIN de salida del filtro asincrónico propone \_ el flujo MEDIATYPE y MEDIASUBTYPE \_ null para el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="980f6-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="980f6-117">El PIN de entrada en el filtro de divisor de AVI no acepta MEDIASUBTYPE \_ null y no propone ningún tipo propio.</span><span class="sxs-lookup"><span data-stu-id="980f6-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="980f6-118">Por lo tanto, se produce un error en la conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="980f6-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="980f6-119">El filtro Async se podría mejorar para ofrecer MEDIASUBTYPE \_ AVI cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="980f6-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="980f6-120">Por ejemplo, podría examinar el formato de archivo o utilizar la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="980f6-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="980f6-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="980f6-121">Downloading the Sample</span></span>

<span data-ttu-id="980f6-122">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="980f6-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="980f6-123">Este ejemplo se instala en la siguiente ruta de acceso: \[ ejemplos *raíz del SDK* \] \\ \\ filtros DirectShow de multimedia \\ \\ \\ Async.</span><span class="sxs-lookup"><span data-stu-id="980f6-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="980f6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="980f6-124">Related topics</span></span>



[<span data-ttu-id="980f6-125">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="980f6-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



