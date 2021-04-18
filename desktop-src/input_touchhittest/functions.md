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
# <a name="touch-hit-testing-functions"></a>Funciones de pruebas de posicionamiento táctiles

En los temas de esta sección se proporcionan las especificaciones de referencia para [las funciones de prueba de posicionamiento táctil](functions.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Devuelve la puntuación de un polígono como el posible destino táctil (en comparación con todos los demás polígonos que forman una intersección con el área de contacto táctil) y un punto táctil ajustado dentro del polígono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Devuelve la puntuación de un rectángulo como el destino de toque probable, en comparación con el resto de rectángulos que forman una intersección con el área de contacto táctil y un punto de toque ajustado dentro del rectángulo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Devuelve la puntuación de evaluación de proximidad y las coordenadas de punto táctil ajustadas como un valor empaquetado para la devolución de llamada del [mensaje WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) . <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra una ventana para procesar la notificación de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de la prueba de posicionamiento táctil](touchhittest-reference.md)
