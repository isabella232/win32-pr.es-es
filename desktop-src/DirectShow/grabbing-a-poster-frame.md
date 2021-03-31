---
description: Captación de un fotograma de póster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Captación de un fotograma de póster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495773"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="4584c-103">Captación de un fotograma de póster</span><span class="sxs-lookup"><span data-stu-id="4584c-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="4584c-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4584c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4584c-105">En este artículo se describe cómo mostrar un fotograma de póster desde un archivo multimedia digital mediante el objeto de [detección de medios (MediaDet)](media-detector--mediadet.md) proporcionado con los [servicios de edición de DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="4584c-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="4584c-106">El detector de medios es un objeto auxiliar que puede obtener información de formato de un archivo de origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="4584c-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="4584c-107">También puede obtener una imagen de mapa de bits de una secuencia de vídeo en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="4584c-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="4584c-108">Suponiendo que se pueda buscar en el archivo, puede obtener la imagen de cualquier punto del archivo.</span><span class="sxs-lookup"><span data-stu-id="4584c-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="4584c-109">La imagen devuelta siempre tiene el formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="4584c-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="4584c-110">El detector de medios no es un filtro y la aplicación no necesita usar el administrador de gráficos de filtro ni crear un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="4584c-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="4584c-111">Internamente, el detector de medios crea un gráfico de filtros que contiene el [**filtro de enganche de ejemplo**](sample-grabber-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4584c-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="4584c-112">Para obtener un mapa de bits, el detector de medios busca y pone en pausa el gráfico de filtro y, a continuación, recupera el mapa de bits del filtro de enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4584c-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="4584c-113">La aplicación se comunica con el detector de medios a través de la interfaz [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="4584c-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="4584c-114">El detector de medios es un buen ejemplo de encapsulación de un gráfico de filtro dentro de un objeto auxiliar, con el fin de proteger las aplicaciones de los detalles relacionados con los gráficos.</span><span class="sxs-lookup"><span data-stu-id="4584c-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="4584c-115">El detector de medios funciona en dos modos.</span><span class="sxs-lookup"><span data-stu-id="4584c-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="4584c-116">Cuando se crea por primera vez, el detector de medios está en modo de "recopilación de información".</span><span class="sxs-lookup"><span data-stu-id="4584c-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="4584c-117">Puede especificar el nombre de un archivo multimedia y obtener información sobre cada una de las secuencias del archivo, como el tipo de formato, la velocidad de fotogramas o la duración.</span><span class="sxs-lookup"><span data-stu-id="4584c-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="4584c-118">Si el archivo contiene una secuencia de vídeo, puede cambiar el detector de medios al modo "captura de mapa de bits" y recuperar los mapas de bits del origen.</span><span class="sxs-lookup"><span data-stu-id="4584c-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="4584c-119">Sin embargo, una vez hecho esto, no puede volver a cambiar el detector de medios a su modo original; está conectado permanentemente a esa secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4584c-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="4584c-120">Para trabajar con otro flujo u otro archivo, debe crear una nueva instancia del detector de medios.</span><span class="sxs-lookup"><span data-stu-id="4584c-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="4584c-121">En los ejemplos de código de este tutorial se usa la clase **CComPtr** de ATL, que administra automáticamente los recuentos de referencias.</span><span class="sxs-lookup"><span data-stu-id="4584c-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="4584c-122">Si prefiere usar punteros de interfaz sin formato, recuerde liberar todas las interfaces cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="4584c-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="4584c-123">Además, para mayor brevedad, los ejemplos de código omiten gran parte de la comprobación de errores que debe realizar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4584c-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="4584c-124">En código de trabajo, compruebe siempre los valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4584c-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="4584c-125">Este tutorial contiene los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="4584c-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="4584c-126">Paso 1: crear Windows Framework</span><span class="sxs-lookup"><span data-stu-id="4584c-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="4584c-127">Paso 2: agregar un comando de menú para capturar un fotograma de póster</span><span class="sxs-lookup"><span data-stu-id="4584c-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="4584c-128">Paso 3: implementar la función Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="4584c-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="4584c-129">Paso 4: dibujo del mapa de bits en el área cliente</span><span class="sxs-lookup"><span data-stu-id="4584c-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="4584c-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4584c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4584c-131">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4584c-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



