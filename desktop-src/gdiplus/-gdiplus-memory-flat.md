---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funciones de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985154"
---
# <a name="memory-functions"></a><span data-ttu-id="18b39-103">Funciones de memoria</span><span class="sxs-lookup"><span data-stu-id="18b39-103">Memory Functions</span></span>

<span data-ttu-id="18b39-104">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="18b39-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="18b39-105">Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="18b39-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="18b39-106">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="18b39-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="18b39-107">Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="18b39-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="18b39-108">Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="18b39-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="18b39-109">Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="18b39-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="18b39-110">Las siguientes funciones de la API plana están incluidas en la clase [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) de C++.</span><span class="sxs-lookup"><span data-stu-id="18b39-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="18b39-111">Funciones de memoria y métodos contenedores correspondientes</span><span class="sxs-lookup"><span data-stu-id="18b39-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="18b39-112">Función plana</span><span class="sxs-lookup"><span data-stu-id="18b39-112">Flat function</span></span>                                          | <span data-ttu-id="18b39-113">Wrapper (método)</span><span class="sxs-lookup"><span data-stu-id="18b39-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="18b39-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18b39-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b39-115">GpStatus WINGDIPAPI GdipAlloc (tamaño \_ t tamaño)</span><span class="sxs-lookup"><span data-stu-id="18b39-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="18b39-116">**GpStatus WINGDIPAPI GdiplusBase void \* (operador New) (tamaño \_ t de \_ tamaño)**</span><span class="sxs-lookup"><span data-stu-id="18b39-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="18b39-117">Asigna memoria para un objeto GDI+ de Windows.</span><span class="sxs-lookup"><span data-stu-id="18b39-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="18b39-118">GdipAlloc se declara en GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="18b39-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="18b39-119">GpStatus WINGDIPAPI GdipFree (void \* ptr);</span><span class="sxs-lookup"><span data-stu-id="18b39-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="18b39-120">**GpStatus WINGDIPAPI GdiplusBase void (operador Delete) (void \* en \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="18b39-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="18b39-121">Desasigna memoria para un objeto GDI+ de Windows.</span><span class="sxs-lookup"><span data-stu-id="18b39-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="18b39-122">GdipFree se declara en GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="18b39-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
