---
description: El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen profundidades de color diferentes.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Pintar en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e3763291eaa94fdc606e42ea2b3b6e5ead564a5e3bc39b246ad6ac5a206a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037703"
---
# <a name="painting-on-multiple-display-monitors"></a>Pintar en varios monitores de pantalla

El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen profundidades de color diferentes. Normalmente, esto produce buenos resultados, pero puede que no sea óptimo. Por ejemplo, una ventana en dos monitores con profundidades de color muy diferentes podría tener una representación de color deficiente. Además, los monitores con la misma profundidad de color pueden tener formatos de color diferentes, por ejemplo, los colores se podrían codificar con un número diferente de bits o estar ubicados en distintos lugares en el valor de color de un píxel.

Para obtener los mejores resultados para cada uno de los monitores de un controlador de dominio que abarca más de una pantalla, llame a [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) para enumerar los monitores que intersecan con el controlador de dominio y pintar el área de intersección en cada uno de ellos por separado según los atributos de presentación de ese monitor. Vea el ejemplo de [Pintar en un controlador de dominio que abarca varias pantallas.](painting-on-a-dc-that-spans-multiple-displays.md)

Si realiza todo el dibujo en el código **WM \_ PAINT** y si el código **WM \_ PAINT** controla todos los distintos modos de vídeo, debería poder colocar el código **WM \_ PAINT** en **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) con solo unas pocas modificaciones.

 

 



