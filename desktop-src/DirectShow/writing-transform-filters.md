---
description: Escribir filtros de transformación
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Escribir filtros de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002151"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="1943f-103">Escribir filtros de transformación</span><span class="sxs-lookup"><span data-stu-id="1943f-103">Writing Transform Filters</span></span>

<span data-ttu-id="1943f-104">En esta sección se describe cómo escribir un filtro de transformación, definido como un filtro que tiene exactamente un PIN de entrada y un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="1943f-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="1943f-105">Para ilustrar los pasos, en esta sección se describe un filtro de transformación hipotético que genera el vídeo de la longitud de ejecución codificada (RLE).</span><span class="sxs-lookup"><span data-stu-id="1943f-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="1943f-106">No describe el algoritmo de codificación RLE en sí, solo las tareas específicas de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1943f-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="1943f-107">(DirectShow ya proporciona un códec RLE a través del filtro del [compresor AVI](avi-compressor-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="1943f-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="1943f-108">En esta sección se da por supuesto que utilizará la biblioteca de clases base de DirectShow para crear filtros.</span><span class="sxs-lookup"><span data-stu-id="1943f-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="1943f-109">Aunque puede escribir un filtro sin él, se recomienda encarecidamente la biblioteca de clases base.</span><span class="sxs-lookup"><span data-stu-id="1943f-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="1943f-110">Antes de escribir un filtro de transformación, tenga en cuenta si un objeto multimedia de DirectX (DMO) cumplirá sus requisitos.</span><span class="sxs-lookup"><span data-stu-id="1943f-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="1943f-111">DMOs puede hacer muchas de las mismas cosas que los filtros, y el modelo de programación para DMOs es más sencillo.</span><span class="sxs-lookup"><span data-stu-id="1943f-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="1943f-112">Los DMOs se hospedan en DirectShow mediante el filtro de [contenedor de DMO](dmo-wrapper-filter.md) , pero también se pueden usar fuera de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1943f-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="1943f-113">DMOs es ahora la solución recomendada para codificadores y descodificadores.</span><span class="sxs-lookup"><span data-stu-id="1943f-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="1943f-114">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="1943f-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="1943f-115">Paso 1. Elegir una clase base</span><span class="sxs-lookup"><span data-stu-id="1943f-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="1943f-116">Paso 2. Declarar la clase de filtro</span><span class="sxs-lookup"><span data-stu-id="1943f-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="1943f-117">Paso 3. Compatibilidad con la negociación de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="1943f-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="1943f-118">Paso 4. Establecer propiedades de asignador</span><span class="sxs-lookup"><span data-stu-id="1943f-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="1943f-119">Paso 5. Transformar la imagen</span><span class="sxs-lookup"><span data-stu-id="1943f-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="1943f-120">Paso 6. Agregar compatibilidad con COM</span><span class="sxs-lookup"><span data-stu-id="1943f-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="1943f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1943f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1943f-122">Compilar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1943f-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="1943f-123">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1943f-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="1943f-124">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1943f-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



