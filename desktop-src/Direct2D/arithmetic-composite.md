---
title: Efecto compuesto aritmético
description: Use el efecto compuesto aritmético para combinar 2 imágenes usando una suma ponderada de píxeles de las imágenes de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efecto compuesto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996862"
---
# <a name="arithmetic-composite-effect"></a>Efecto compuesto aritmético

Use el efecto compuesto aritmético para combinar 2 imágenes usando una suma ponderada de píxeles de las imágenes de entrada.

El CLSID para este efecto es CLSID \_ D2D1ArithmeticComposite.

-   [Fórmula](#formula)
-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="formula"></a>Fórmula

La fórmula aquí se usa para calcular este efecto.

Salida<sub>RGBA</sub> = origen de código C1 de \* destino<sub>RGBA</sub> \* + origen de C2<sub></sub> \* <sub>RGBA</sub> + C3 \* destino<sub>RGBA</sub> + C4

Donde C1, C2, C3, C4 son coeficientes que se establecen.

Los coeficientes se asignan a los valores de un D2D1 \_ Vector \_ 4F (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Imagen de ejemplo

Un ejemplo sencillo es agregar los píxeles de origen y de destino. En el ejemplo, se componen dos rectángulos redondeados. El rectángulo de origen es azul y el destino es rojo.

La imagen siguiente es la salida del efecto compuesto aritmético con los coeficientes de la ecuación establecida en los valores aquí.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![imagen de ejemplo que muestra dos rectángulos redondeados del mismo tamaño que se superponen con el efecto compuesto aritmético.](images/arithmetic-50-percent.png)

El resultado es que se agregan los valores de píxel para el origen y el destino. Las regiones en las que los rectángulos no se superponen los valores RGBA son 0. Donde los rectángulos se superponen el color es magenta porque los valores R y B están en el máximo.

Esta es otra imagen de ejemplo con el código.



| Antes de la imagen 1                                                             |
|----------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| Antes de la imagen 2                                                             |
| ![segunda imagen anterior al efecto.](images/4-arthimetic-composite2.jpg) |
| Después                                                                      |
| ![la imagen después de la transformación.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficientes<br/> Coeficientes de D2D1 \_ ARITHMETICCOMPOSITE \_ \_<br/> | Coeficientes para la ecuación que se usa para componer las dos imágenes de entrada. Los coeficientes son sin unidades y sin límite. El tipo es D2D1 \_ Vector \_ 4F.<br/> El valor predeterminado es {1,0 f, 0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ ARITHMETICCOMPOSITE \_ \_ \_<br/> | El efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. <br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El mapa de bits de salida depende de los valores de coeficiente. Estos son los posibles tamaños de mapa de bits de salida.

-   Si C1 es el único coeficiente distinto de cero, el tamaño de salida es la intersección de los rectángulos de entrada.
-   Si C2 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo de origen.
-   Si C3 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo de destino.
-   Si todos los coeficientes son cero, el tamaño de salida es un rectángulo vacío.
-   Para todos los demás valores de coeficiente, el tamaño de salida es la Unión de los rectángulos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

