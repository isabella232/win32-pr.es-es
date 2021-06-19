---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase Brush de C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funciones brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395090"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="88dba-104">Funciones brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="88dba-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="88dba-105">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="88dba-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="88dba-106">Las funciones de la API plana de GDI+ están encapsuladas por una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="88dba-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="88dba-107">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="88dba-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="88dba-108">Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="88dba-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="88dba-109">Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="88dba-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="88dba-110">Para obtener más información sobre el uso de estos métodos contenedor, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="88dba-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="88dba-111">Las siguientes funciones de API planas se encapsulan mediante la [**clase Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) de C++.</span><span class="sxs-lookup"><span data-stu-id="88dba-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="88dba-112">Funciones brush y métodos contenedor correspondientes</span><span class="sxs-lookup"><span data-stu-id="88dba-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="88dba-113">Función plana</span><span class="sxs-lookup"><span data-stu-id="88dba-113">Flat function</span></span>                                                                        | <span data-ttu-id="88dba-114">Método contenedor</span><span class="sxs-lookup"><span data-stu-id="88dba-114">Wrapper method</span></span>                                          | <span data-ttu-id="88dba-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="88dba-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dba-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \* brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="88dba-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="88dba-117">**Brush::Clone**</span><span class="sxs-lookup"><span data-stu-id="88dba-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="88dba-118">El [**método Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuevo [**objeto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basado en este pincel.</span><span class="sxs-lookup"><span data-stu-id="88dba-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="88dba-119">GpStatus WINGDIPAPI GdipDeleteBrush(Pincel \* GpBrush)</span><span class="sxs-lookup"><span data-stu-id="88dba-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="88dba-120">virtual ~Brush()</span><span class="sxs-lookup"><span data-stu-id="88dba-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="88dba-121">Limpia los recursos utilizados por un [**objeto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)</span><span class="sxs-lookup"><span data-stu-id="88dba-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="88dba-122">GpStatus WINGDIPAPI GdipGetBrushType(pincel \* GpBrush, tipo \* GpBrushType)</span><span class="sxs-lookup"><span data-stu-id="88dba-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="88dba-123">**Brush::GetType**</span><span class="sxs-lookup"><span data-stu-id="88dba-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="88dba-124">El [**método Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtiene el tipo de este pincel.</span><span class="sxs-lookup"><span data-stu-id="88dba-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




