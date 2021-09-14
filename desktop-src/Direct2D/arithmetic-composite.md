---
title: Efecto compuesto aritmético
description: Use el efecto compuesto aritmético para combinar dos imágenes con una suma ponderada de píxeles de las imágenes de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efecto compuesto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164257"
---
# <a name="arithmetic-composite-effect"></a>Efecto compuesto aritmético

Use el efecto compuesto aritmético para combinar dos imágenes con una suma ponderada de píxeles de las imágenes de entrada.

El CLSID para este efecto es CLSID \_ D2D1ArithmeticComposite.

-   [Fórmula](#formula)
-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="formula"></a>Fórmula

La fórmula aquí se usa para calcular este efecto.

Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4

Donde C1, C2, C3, C4 son coeficientes que se establecen.

Los coeficientes se asignan a los valores de D2D1 \_ VECTOR \_ 4F (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Imagen de ejemplo

Un ejemplo sencillo es agregar los píxeles de origen y destino. En el ejemplo, dos rectángulos redondeados se composiciónn juntos. El rectángulo de origen es azul y el destino es rojo.

La imagen aquí es la salida del efecto Compuesto aritmético con los coeficientes de la ecuación establecidos en los valores aquí.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![una imagen de ejemplo que muestra 2 rectángulos redondeados del mismo tamaño que se superponen mediante el efecto compuesto aritmético.](images/arithmetic-50-percent.png)

El resultado es que se agregan los valores de píxeles para el origen y el destino. Las regiones en las que los rectángulos no se superponen a los valores RGBA son todas 0. Cuando los rectángulos se superponen, el color es de color azul azulado porque los valores de R y B están al máximo.

Esta es otra imagen de ejemplo con código.



| Antes de la imagen 1                                                             |
|----------------------------------------------------------------------------|
| ![la primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| Antes de la imagen 2                                                             |
| ![la segunda imagen antes del efecto.](images/4-arthimetic-composite2.jpg) |
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



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficientes<br/> D2D1 \_ ARITHMETICCOMPOSITE \_ PROP \_ COEFFICIENTS<br/> | Coeficientes de la ecuación utilizada para componer las dos imágenes de entrada. Los coeficientes son sin unidad y sin enlazar. El tipo es D2D1 \_ VECTOR \_ 4F.<br/> El valor predeterminado es {1.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN DE PROP DE D2D1 \_ ARITHMETICCOMPOSITE \_ \_ \_<br/> | El efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. <br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El mapa de bits de salida depende de los valores del coeficiente. Estos son los posibles tamaños de mapa de bits de salida.

-   Si C1 es el único coeficiente distinto de cero, el tamaño de salida es la intersección de los rectángulos de entrada.
-   Si C2 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo Origen.
-   Si C3 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo Destino.
-   Si todos los coeficientes son cero, el tamaño de salida es un rectángulo vacío.
-   Para todos los demás valores de coeficiente, el tamaño de salida es la unión de los rectángulos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

