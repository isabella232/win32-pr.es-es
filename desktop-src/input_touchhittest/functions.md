---
title: Funciones (prueba de posicionamiento táctil)
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de prueba de posicionamiento táctil.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interacción con el usuario
- input
- puntero
- Función táctil
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721640"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="ebbc4-107">Funciones de pruebas de posicionamiento táctiles</span><span class="sxs-lookup"><span data-stu-id="ebbc4-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="ebbc4-108">En los temas de esta sección se proporcionan las especificaciones de referencia para [las funciones de prueba de posicionamiento táctil](functions.md).</span><span class="sxs-lookup"><span data-stu-id="ebbc4-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebbc4-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ebbc4-109">In this section</span></span>

| <span data-ttu-id="ebbc4-110">Tema</span><span class="sxs-lookup"><span data-stu-id="ebbc4-110">Topic</span></span> | <span data-ttu-id="ebbc4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebbc4-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="ebbc4-112">**EvaluateProximityToPolygon**</span><span class="sxs-lookup"><span data-stu-id="ebbc4-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="ebbc4-113">Devuelve la puntuación de un polígono como el posible destino táctil (en comparación con todos los demás polígonos que forman una intersección con el área de contacto táctil) y un punto táctil ajustado dentro del polígono.</span><span class="sxs-lookup"><span data-stu-id="ebbc4-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="ebbc4-114">**EvaluateProximityToRect**</span><span class="sxs-lookup"><span data-stu-id="ebbc4-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="ebbc4-115">Devuelve la puntuación de un rectángulo como el destino de toque probable, en comparación con el resto de rectángulos que forman una intersección con el área de contacto táctil y un punto de toque ajustado dentro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ebbc4-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="ebbc4-116">**PackTouchHitTestingProximityEvaluation**</span><span class="sxs-lookup"><span data-stu-id="ebbc4-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="ebbc4-117">Devuelve la puntuación de evaluación de proximidad y las coordenadas de punto táctil ajustadas como un valor empaquetado para la devolución de llamada del [mensaje WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) .</span><span class="sxs-lookup"><span data-stu-id="ebbc4-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="ebbc4-118">**RegisterTouchHitTestingWindow**</span><span class="sxs-lookup"><span data-stu-id="ebbc4-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="ebbc4-119">Registra una ventana para procesar la notificación de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)</span><span class="sxs-lookup"><span data-stu-id="ebbc4-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="ebbc4-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebbc4-120">Related topics</span></span>

[<span data-ttu-id="ebbc4-121">Referencia de la prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="ebbc4-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
