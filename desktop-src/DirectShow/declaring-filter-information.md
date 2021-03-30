---
description: Declarar información de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarar información de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806709"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="c7682-103">Declarar información de filtro</span><span class="sxs-lookup"><span data-stu-id="c7682-103">Declaring Filter Information</span></span>

<span data-ttu-id="c7682-104">El primer paso consiste en declarar la información de filtro, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c7682-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="c7682-105">DirectShow define las siguientes estructuras para describir los filtros, los pin y los tipos de medios:</span><span class="sxs-lookup"><span data-stu-id="c7682-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="c7682-106">Estructura</span><span class="sxs-lookup"><span data-stu-id="c7682-106">Structure</span></span>                                               | <span data-ttu-id="c7682-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7682-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c7682-108">**filtro de AMOVIESETUP \_**</span><span class="sxs-lookup"><span data-stu-id="c7682-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="c7682-109">Describe un filtro.</span><span class="sxs-lookup"><span data-stu-id="c7682-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="c7682-110">**AMOVIESETUP \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="c7682-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="c7682-111">Describe un código PIN.</span><span class="sxs-lookup"><span data-stu-id="c7682-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="c7682-112">**AMOVIESETUP \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="c7682-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="c7682-113">Describe un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c7682-113">Describes a media type.</span></span> |



 

<span data-ttu-id="c7682-114">Estas estructuras están anidadas.</span><span class="sxs-lookup"><span data-stu-id="c7682-114">These structures are nested.</span></span> <span data-ttu-id="c7682-115">La estructura de **\_ filtro AMOVEIESETUP** tiene un puntero a una matriz de estructuras **AMOVIESETUP \_ PIN** y cada una de ellas tiene un puntero a una matriz de estructuras **AMOVEIESETUP \_ MEDIATYPE** .</span><span class="sxs-lookup"><span data-stu-id="c7682-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="c7682-116">En conjunto, estas estructuras proporcionan información suficiente para que la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) busque un filtro.</span><span class="sxs-lookup"><span data-stu-id="c7682-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="c7682-117">No se trata de una descripción completa de un filtro.</span><span class="sxs-lookup"><span data-stu-id="c7682-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="c7682-118">Por ejemplo, si el filtro crea varias instancias del mismo pin, debe declarar solo una estructura de [**\_ PIN AMOVIESETUP**](amoviesetup-pin.md) para ese pin.</span><span class="sxs-lookup"><span data-stu-id="c7682-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="c7682-119">Además, no es necesario que un filtro admita cada combinación de tipos de medios que registra. no es necesario para registrar todos los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="c7682-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="c7682-120">Declare las estructuras de configuración como variables globales en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c7682-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="c7682-121">En el ejemplo siguiente se muestra un filtro con un PIN de salida:</span><span class="sxs-lookup"><span data-stu-id="c7682-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="c7682-122">El nombre del filtro se declara como una variable global estática, porque se utilizará de nuevo en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="c7682-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7682-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7682-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7682-124">Cómo registrar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7682-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



