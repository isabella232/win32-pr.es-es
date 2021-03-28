---
description: Un rectángulo es un polígono de cuatro lados cuyos lados opuestos son paralelos y tienen la misma longitud.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Dibujar rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908491"
---
# <a name="drawing-rectangles"></a>Dibujar rectángulos

Un rectángulo es un polígono de cuatro lados cuyos lados opuestos son paralelos y tienen la misma longitud. Aunque una aplicación puede dibujar un rectángulo mediante una llamada a la función [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , proporcionando las coordenadas de cada esquina, la función de [**rectángulo**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) proporciona un método más sencillo. Esta función solo requiere las coordenadas de la esquina superior izquierda y la esquina inferior derecha. Cuando una aplicación llama a la función de [**rectángulo**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , el sistema dibuja el rectángulo, excluyendo los lados derecho e inferior si no se establece ninguna transformación universal para el contexto de dispositivo especificado.

Si se ha establecido una transformación universal mediante la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , el sistema incluye los bordes derecho e inferior.

Además de dibujar un rectángulo tradicional, puede dibujar rectángulos con esquinas redondeadas. La función [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) requiere que la aplicación proporcione las coordenadas de las esquinas inferior izquierda y superior derecha, así como el ancho y el alto de la elipse que se usa para redondear cada esquina.

Las aplicaciones pueden utilizar las siguientes funciones para manipular los rectángulos.



| Función                         | Descripción                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | Vuelve a dibujar el interior de un rectángulo.                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | Vuelve a dibujar los lados de un rectángulo.                                  |
| [**InvertRect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | Invierte los colores que aparecen dentro del interior de un rectángulo. |



 

 

 
