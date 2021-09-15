---
title: Funciones (prueba de impacto táctil)
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de prueba de impacto táctil.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interacción con el usuario
- input
- puntero
- Función táctil
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569169"
---
# <a name="touch-hit-testing-functions"></a>Funciones de prueba de impacto táctil

En los temas de esta sección se proporcionan las especificaciones de referencia para las [funciones de prueba de impacto táctil](functions.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Devuelve la puntuación de un polígono como destino táctil probable (en comparación con todos los demás polígonos que intersecan con el área de contacto táctil) y un punto táctil ajustado dentro del polígono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Devuelve la puntuación de un rectángulo como destino táctil probable, en comparación con todos los demás rectángulos que cruzan el área de contacto táctil y un punto táctil ajustado dentro del rectángulo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Devuelve la puntuación de evaluación de proximidad y las coordenadas de punto táctil ajustadas como un valor empaquetado para la devolución WM_TOUCHHITTESTING [de llamada del](../inputmsg/wm-touchhittesting.md) mensaje. <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra una ventana para procesar la [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notificación<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de pruebas de impacto táctiles](touchhittest-reference.md)
