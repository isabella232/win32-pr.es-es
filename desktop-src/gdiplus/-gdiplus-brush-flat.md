---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funciones de pincel (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360620"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="5a74d-103">Funciones de pincel (GDI+)</span><span class="sxs-lookup"><span data-stu-id="5a74d-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="5a74d-104">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="5a74d-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="5a74d-105">Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="5a74d-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="5a74d-106">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="5a74d-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="5a74d-107">Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="5a74d-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="5a74d-108">Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="5a74d-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="5a74d-109">Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="5a74d-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="5a74d-110">Las siguientes funciones de la API sin formato se ajustan mediante la clase de C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="5a74d-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="5a74d-111">Funciones de pincel y métodos contenedores correspondientes</span><span class="sxs-lookup"><span data-stu-id="5a74d-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="5a74d-112">Función plana</span><span class="sxs-lookup"><span data-stu-id="5a74d-112">Flat function</span></span>                                                                        | <span data-ttu-id="5a74d-113">Wrapper (método)</span><span class="sxs-lookup"><span data-stu-id="5a74d-113">Wrapper method</span></span>                                          | <span data-ttu-id="5a74d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a74d-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a74d-115">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="5a74d-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="5a74d-116">**Brush:: Clone**</span><span class="sxs-lookup"><span data-stu-id="5a74d-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="5a74d-117">El método [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuevo objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basado en este pincel.</span><span class="sxs-lookup"><span data-stu-id="5a74d-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="5a74d-118">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)</span><span class="sxs-lookup"><span data-stu-id="5a74d-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="5a74d-119">Pincel ~ de virtual ()</span><span class="sxs-lookup"><span data-stu-id="5a74d-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="5a74d-120">Limpia los recursos usados por un objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="5a74d-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="5a74d-121">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* Type)</span><span class="sxs-lookup"><span data-stu-id="5a74d-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="5a74d-122">**Brush:: GetType**</span><span class="sxs-lookup"><span data-stu-id="5a74d-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="5a74d-123">El método [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtiene el tipo de este pincel.</span><span class="sxs-lookup"><span data-stu-id="5a74d-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




