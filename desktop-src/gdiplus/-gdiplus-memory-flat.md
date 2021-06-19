---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. La clase GdiplusBase de C++ encapsula estas funciones de API planas.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funciones de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395830"
---
# <a name="memory-functions"></a><span data-ttu-id="3b760-104">Funciones de memoria</span><span class="sxs-lookup"><span data-stu-id="3b760-104">Memory Functions</span></span>

<span data-ttu-id="3b760-105">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="3b760-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="3b760-106">Las funciones de la API plana de GDI+ están encapsuladas por una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="3b760-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="3b760-107">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="3b760-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="3b760-108">Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="3b760-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="3b760-109">Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="3b760-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="3b760-110">Para obtener más información sobre el uso de estos métodos contenedor, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="3b760-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="3b760-111">La clase [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) de C++ encapsula las siguientes funciones de API planas.</span><span class="sxs-lookup"><span data-stu-id="3b760-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="3b760-112">Funciones de memoria y métodos contenedor correspondientes</span><span class="sxs-lookup"><span data-stu-id="3b760-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="3b760-113">Función plana</span><span class="sxs-lookup"><span data-stu-id="3b760-113">Flat function</span></span>                                          | <span data-ttu-id="3b760-114">Método contenedor</span><span class="sxs-lookup"><span data-stu-id="3b760-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="3b760-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b760-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b760-116">GpStatus WINGDIPAPI GdipAlloc(tamaño \_ t)</span><span class="sxs-lookup"><span data-stu-id="3b760-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="3b760-117">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**</span><span class="sxs-lookup"><span data-stu-id="3b760-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="3b760-118">Asigna memoria para un objeto GDI+ de Windows.</span><span class="sxs-lookup"><span data-stu-id="3b760-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="3b760-119">GdipAlloc se declara en GdiplusMem.h.</span><span class="sxs-lookup"><span data-stu-id="3b760-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="3b760-120">GpStatus WINGDIPAPI GdipFree(void \* ptr);</span><span class="sxs-lookup"><span data-stu-id="3b760-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="3b760-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="3b760-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="3b760-122">Desasigna la memoria de un objeto GDI+ de Windows.</span><span class="sxs-lookup"><span data-stu-id="3b760-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="3b760-123">GdipFree se declara en GdiplusMem.h.</span><span class="sxs-lookup"><span data-stu-id="3b760-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
