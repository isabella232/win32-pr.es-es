---
title: Uso de rectángulos (Reproductor de Windows Media SDK)
description: Usar rectángulos
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizaciones, rectángulos
- visualizaciones personalizadas, rectángulos
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dd46928ccf8f8a0a465fa71fbb6b1bc1b4f48cbdb5c37b4b93ffd21c78c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117300"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Uso de rectángulos (Reproductor de Windows Media SDK)

Los rectángulos se usan para especificar áreas rectangulares en Microsoft Windows. Puede crear muchos rectángulos en la ventana, pero Reproductor de Windows Media proporciona los valores de un rectángulo a través de la función [IWMPEffects::Render.](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) Si el complemento se representa mediante una ventana, el rectángulo es el área cliente de la ventana. Esto se denomina rectángulo prc y define el rectángulo que Reproductor de Windows Media mostrará la visualización. Úsese esto con frecuencia para asegurarse de que no se dibuja más allá de las extensiones del rectángulo proporcionado por Reproductor de Windows Media.

Un rectángulo tiene cuatro valores que lo definen. Son izquierda, superior, derecha e inferior. La esquina superior izquierda del rectángulo se define por la izquierda y la parte superior, y la esquina inferior derecha del rectángulo se define por abajo y derecha.

Use el código siguiente para obtener las extensiones del rectángulo de dibujo. Debe hacerlo porque el usuario puede cambiar el tamaño de la ventana y desea asegurarse de que siempre dibuja en un área que el usuario puede ver.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Por ejemplo, para dibujar de izquierda a derecha, en la parte superior de la ventana, use código como este:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de Render**](implementing-render.md)
</dt> </dl>

 

 




