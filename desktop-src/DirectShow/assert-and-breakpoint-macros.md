---
description: Macros Assert y Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert y Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152612"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="278a2-103">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="278a2-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="278a2-104">Las [clases base de DirectShow](directshow-base-classes.md) proporcionan varias macros que realizan aserciones o causan puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="278a2-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="278a2-105">Macro</span><span class="sxs-lookup"><span data-stu-id="278a2-105">Macro</span></span>                                        | <span data-ttu-id="278a2-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="278a2-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="278a2-107">**DECLARAR**</span><span class="sxs-lookup"><span data-stu-id="278a2-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="278a2-108">Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="278a2-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="278a2-109">**DbgAssertAligned**</span><span class="sxs-lookup"><span data-stu-id="278a2-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="278a2-110">Comprueba si un puntero está alineado con un límite especificado.</span><span class="sxs-lookup"><span data-stu-id="278a2-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="278a2-111">**DbgBreak**</span><span class="sxs-lookup"><span data-stu-id="278a2-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="278a2-112">Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="278a2-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="278a2-113">**EJECUTAR \_ aserción**</span><span class="sxs-lookup"><span data-stu-id="278a2-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="278a2-114">Evalúa una expresión en las compilaciones de depuración y comerciales.</span><span class="sxs-lookup"><span data-stu-id="278a2-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="278a2-115">En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="278a2-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="278a2-116">**KASSERT**</span><span class="sxs-lookup"><span data-stu-id="278a2-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="278a2-117">Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="278a2-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="278a2-118">**KDbgBreak**</span><span class="sxs-lookup"><span data-stu-id="278a2-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="278a2-119">Produce una excepción de punto de interrupción y registra la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="278a2-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="278a2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="278a2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278a2-121">Herramientas de depuración</span><span class="sxs-lookup"><span data-stu-id="278a2-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



