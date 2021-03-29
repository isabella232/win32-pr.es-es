---
title: Interoperar con GDI
description: DirectWrite proporciona una ruta de migración desde, y alguna interoperabilidad con, modelo de fuente de GDI, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, interoperación GDI
- DirectWrite, interoperabilidad
- interoperabilidad
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077794"
---
# <a name="interoperating-with-gdi"></a><span data-ttu-id="693fc-108">Interoperar con GDI</span><span class="sxs-lookup"><span data-stu-id="693fc-108">Interoperating with GDI</span></span>

<span data-ttu-id="693fc-109">[DirectWrite](direct-write-portal.md) proporciona una ruta de migración desde, y alguna interoperabilidad con, modelo de fuente de GDI, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.</span><span class="sxs-lookup"><span data-stu-id="693fc-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="693fc-110">Esta información general contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="693fc-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="693fc-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="693fc-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="693fc-112">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="693fc-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="693fc-113">Parte 2: objetos de fuente</span><span class="sxs-lookup"><span data-stu-id="693fc-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="693fc-114">Parte 3: representación</span><span class="sxs-lookup"><span data-stu-id="693fc-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="693fc-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="693fc-115">Introduction</span></span>

<span data-ttu-id="693fc-116">[DirectWrite](direct-write-portal.md) proporciona métodos para la conversión entre la estructura LOGFONT de GDI y las interfaces de fuente de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="693fc-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="693fc-117">Esto le permite usar GDI para algunas o todas las enumeraciones y selección de fuentes, a la vez que aprovecha la funcionalidad mejorada y el rendimiento de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="693fc-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="693fc-118">DirectWrite también tiene interfaces para representar en un mapa de bits si desea mostrar texto en una superficie de GDI.</span><span class="sxs-lookup"><span data-stu-id="693fc-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="693fc-119">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="693fc-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="693fc-120">La interfaz [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) se usa para convertir entre estructuras de fuentes de GDI e interfaces de fuente de [DirectWrite](direct-write-portal.md) , y también para crear un objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="693fc-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="693fc-121">Obtenga un objeto **IDWriteGdiInterop** mediante el método [**IDWriteFactory:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="693fc-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="693fc-122">Parte 2: objetos de fuente</span><span class="sxs-lookup"><span data-stu-id="693fc-122">Part 2: Font Objects</span></span>

<span data-ttu-id="693fc-123">GDI utiliza la estructura LOGFONT para almacenar información sobre la fuente y el estilo del texto.</span><span class="sxs-lookup"><span data-stu-id="693fc-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="693fc-124">El método [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) convertirá una estructura LOGFONT en un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , como se aprecia en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="693fc-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="693fc-125">Sin embargo, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) no encapsula toda la información que realiza un LogFont.</span><span class="sxs-lookup"><span data-stu-id="693fc-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="693fc-126">Una estructura LOGFONT contiene el tamaño de fuente, el peso, el estilo, el subrayado, el tachado, el nombre de la fuente y otro tipo de información.</span><span class="sxs-lookup"><span data-stu-id="693fc-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="693fc-127">Los objetos **IDWriteFont** contienen información sobre una fuente y su peso y estilo, pero no el tamaño de fuente, el subrayado, etc.</span><span class="sxs-lookup"><span data-stu-id="693fc-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="693fc-128">Con [DirectWrite](direct-write-portal.md), los elementos de información de formato, como estos, se encapsulan con un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o, para rangos de texto concretos, un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="693fc-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="693fc-129">Tiene la opción de convertir un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) en LOGFONT mediante [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span><span class="sxs-lookup"><span data-stu-id="693fc-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="693fc-130">Parte 3: representación</span><span class="sxs-lookup"><span data-stu-id="693fc-130">Part 3: Rendering</span></span>

<span data-ttu-id="693fc-131">Para representar el texto de DirectWrite en una superficie de GDI, se usa un representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="693fc-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="693fc-132">Vea el tema [representar en una superficie de GDI](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="693fc-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 