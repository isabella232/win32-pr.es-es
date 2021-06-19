---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase solidBrush de C++.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funciones SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395560"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="3bca6-104">Funciones SolidBrush</span><span class="sxs-lookup"><span data-stu-id="3bca6-104">SolidBrush Functions</span></span>

<span data-ttu-id="3bca6-105">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="3bca6-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="3bca6-106">Las funciones de la API plana de GDI+ se encapsulan mediante una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="3bca6-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="3bca6-107">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="3bca6-107">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="3bca6-108">Siempre que realice llamadas a GDI+, se recomienda que lo haga llamando a los métodos y funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="3bca6-108">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="3bca6-109">Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="3bca6-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="3bca6-110">Para obtener más información sobre el uso de estos métodos de contenedor, vea [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="3bca6-110">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="3bca6-111">Las siguientes funciones de API planas se encapsulan mediante la [**clase solidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) de C++.</span><span class="sxs-lookup"><span data-stu-id="3bca6-111">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="3bca6-112">Funciones brush y métodos contenedores correspondientes</span><span class="sxs-lookup"><span data-stu-id="3bca6-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="3bca6-113">Función plana</span><span class="sxs-lookup"><span data-stu-id="3bca6-113">Flat function</span></span>                                                                               | <span data-ttu-id="3bca6-114">Método de contenedor</span><span class="sxs-lookup"><span data-stu-id="3bca6-114">Wrapper method</span></span>                                                                                       | <span data-ttu-id="3bca6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bca6-115">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bca6-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(color ARGB, pincel GpSolidFill) \* \***</span><span class="sxs-lookup"><span data-stu-id="3bca6-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="3bca6-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="3bca6-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="3bca6-118">Crea un [**objeto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basado en un color</span><span class="sxs-lookup"><span data-stu-id="3bca6-118">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="3bca6-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(Pincel GpSolidFill, \* color ARGB)**</span><span class="sxs-lookup"><span data-stu-id="3bca6-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="3bca6-120">**SolidBrush::SetColor(IN const Color& color)**</span><span class="sxs-lookup"><span data-stu-id="3bca6-120">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="3bca6-121">Establece el color de este pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="3bca6-121">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="3bca6-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(Pincel GpSolidFill, \* \* color ARGB)**</span><span class="sxs-lookup"><span data-stu-id="3bca6-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="3bca6-123">**SolidBrush::GetColor(OUT Color \* color) const**</span><span class="sxs-lookup"><span data-stu-id="3bca6-123">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="3bca6-124">Obtiene el color de este pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="3bca6-124">Gets the color of this solid brush</span></span>                                                      |



 

 

 
