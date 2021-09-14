---
description: Use la función GetDC para llevar a cabo el dibujo que debe producirse al instante en lugar de cuando se procesa un \_ mensaje WM PAINT.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Uso de la función GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248691"
---
# <a name="using-the-getdc-function"></a>Uso de la función GetDC

Use la función [**GetDC para**](/windows/desktop/api/Winuser/nf-winuser-getdc) llevar a cabo el dibujo que debe producirse al instante en lugar de cuando se procesa un mensaje [**WM \_ PAINT.**](wm-paint.md) Este dibujo suele ser en respuesta a una acción del usuario, como realizar una selección o dibujar con el mouse. En tales casos, el usuario debe recibir comentarios instantáneos y no debe ser forzado a dejar de seleccionar o dibujar para que la aplicación muestre el resultado. En las secciones siguientes se muestra cómo usar GetDC para dibujar en una ventana:

-   [Dibujo con el mouse](drawing-with-the-mouse.md)
-   [Dibujo a intervalos de tiempo](drawing-at-timed-intervals.md)

 

 



