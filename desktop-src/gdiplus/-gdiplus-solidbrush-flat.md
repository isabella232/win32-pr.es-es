---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush (funciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984434"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="fd569-103">SolidBrush (funciones)</span><span class="sxs-lookup"><span data-stu-id="fd569-103">SolidBrush Functions</span></span>

<span data-ttu-id="fd569-104">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="fd569-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="fd569-105">Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="fd569-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="fd569-106">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="fd569-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="fd569-107">Siempre que realice llamadas a GDI+, recomendamos que lo haga llamando a los métodos y las funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="fd569-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="fd569-108">Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="fd569-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="fd569-109">Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="fd569-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="fd569-110">Las siguientes funciones de la API plana están incluidas en la clase de C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .</span><span class="sxs-lookup"><span data-stu-id="fd569-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="fd569-111">Funciones de pincel y métodos contenedores correspondientes</span><span class="sxs-lookup"><span data-stu-id="fd569-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="fd569-112">Función plana</span><span class="sxs-lookup"><span data-stu-id="fd569-112">Flat function</span></span>                                                                               | <span data-ttu-id="fd569-113">Wrapper (método)</span><span class="sxs-lookup"><span data-stu-id="fd569-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="fd569-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd569-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd569-115">**GpStatus WINGDIPAPI GdipCreateSolidFill (color ARGB, GpSolidFill \* \* Brush)**</span><span class="sxs-lookup"><span data-stu-id="fd569-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="fd569-116">[**SolidBrush:: SolidBrush (en el color const& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="fd569-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="fd569-117">Crea un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basado en un color.</span><span class="sxs-lookup"><span data-stu-id="fd569-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="fd569-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, color ARGB)**</span><span class="sxs-lookup"><span data-stu-id="fd569-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="fd569-119">**SolidBrush:: SetColor (en el color const& color)**</span><span class="sxs-lookup"><span data-stu-id="fd569-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="fd569-120">Establece el color de este pincel sólido</span><span class="sxs-lookup"><span data-stu-id="fd569-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="fd569-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, \* color ARGB)**</span><span class="sxs-lookup"><span data-stu-id="fd569-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="fd569-122">**SolidBrush:: GetColor (color de salida \* del color) Const**</span><span class="sxs-lookup"><span data-stu-id="fd569-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="fd569-123">Obtiene el color de este pincel sólido</span><span class="sxs-lookup"><span data-stu-id="fd569-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
