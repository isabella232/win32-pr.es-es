---
title: Usar rectángulos (SDK de Windows Media Player)
description: Usar rectángulos
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizaciones, rectángulos
- visualizaciones personalizadas, rectángulos
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705109"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Usar rectángulos (SDK de Windows Media Player)

Los rectángulos se usan para especificar áreas rectangulares en Microsoft Windows. Puede crear muchos rectángulos en la ventana, pero Windows Media Player proporciona los valores de un rectángulo a través de la función [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) . Si el complemento se representa mediante una ventana, el rectángulo es el área cliente de la ventana. Esto se denomina rectángulo PRC y define el rectángulo en el que Windows Media Player mostrará la visualización. Úselo con frecuencia para asegurarse de que no se dibuja más allá de las extensiones del rectángulo proporcionado por Windows Media Player.

Un rectángulo tiene cuatro valores que lo definen. Son izquierda, superior, derecha e inferior. La esquina superior izquierda del rectángulo se define por la izquierda y la parte superior, y la esquina inferior derecha del rectángulo se define por la parte inferior y derecha.

Use el código siguiente para obtener las extensiones del rectángulo del dibujo. Debe hacerlo porque el usuario puede cambiar el tamaño de la ventana y desea asegurarse de que siempre dibuja en un área que el usuario puede ver.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Por ejemplo, para dibujar de izquierda a derecha, a lo largo de la parte superior de la ventana, use código similar al siguiente:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de render**](implementing-render.md)
</dt> </dl>

 

 




