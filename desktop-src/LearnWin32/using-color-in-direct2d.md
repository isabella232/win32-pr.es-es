---
title: Uso de color en Direct2D
description: Uso de color en Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159931"
---
# <a name="using-color-in-direct2d"></a>Uso de color en Direct2D

Direct2D usa el modelo de color RGB, en el que los colores se forman combinando diferentes valores de rojo, verde y azul. Un cuarto componente, alfa, mide la transparencia de un píxel. En Direct2D, cada uno de estos componentes es un valor de punto flotante con un intervalo de \[ 0,0 1,0 \] . Para los tres componentes de color, el valor mide la intensidad del color. Para el componente alfa, 0,0 significa completamente transparente y 1,0 significa completamente opaco. En la tabla siguiente se muestran los colores resultantes de varias combinaciones de intensidad del 100 %.



| Rojo | Verde | Azul | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Negro   |
| 1   | 0     | 0    | Rojo     |
| 0   | 1     | 0    | Verde   |
| 0   | 0     | 1    | Azul    |
| 0   | 1     | 1    | Cian    |
| 1   | 0     | 1    | Fucsia |
| 1   | 1     | 0    | Amarillo  |
| 1   | 1     | 1    | Blanco   |



 

![una imagen que muestra los colores rgb.](images/graphics13.png)

Los valores de color entre 0 y 1 tienen como resultado diferentes tonalidades de estos colores puros. Direct2D usa la [**estructura D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f) para representar colores. Por ejemplo, el código siguiente especifica el parámetro qr.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



También puede especificar un color mediante la clase [**D2D1::ColorF,**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) que se deriva de la estructura [**D2D1 \_ COLOR \_ F.**](/windows/desktop/Direct2D/d2d1-color-f)


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Combinación alfa

La combinación alfa crea áreas translúcidas combinando el color de primer plano con el color de fondo, mediante la fórmula siguiente.

<dl> color = af * Cf + (1 - af) * Cb  
</dl>

donde *Cb* es el color de fondo, *Cf* es el color de primer plano y *af* es el valor alfa del color de primer plano. Esta fórmula se aplica en pares a cada componente de color. Por ejemplo, suponga que el color de primer plano es **(R = 1,0, G = 0,4, B = 0,0)**, con **alpha = 0,6** y el color de fondo es **(R = 0,0, G = 0,5, B = 1,0).** El color combinado alfa resultante es:

R = (1,0 * 0,6 + 0 * 0,4) = .6   
G = (0,4 * 0,6 + 0,5 * 0,4) = .44  
B = (0 * 0,6 + 1,0 * 0,4) = .40  

En la imagen siguiente se muestra el resultado de esta operación de combinación.

![una imagen que muestra la combinación alfa.](images/graphics15.png)

## <a name="pixel-formats"></a>Formatos de píxel

La [**estructura D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f) no describe cómo se representa un píxel en la memoria. En la mayoría de los casos, eso no importa. Direct2D controla todos los detalles internos de la traducción de información de color en píxeles. Pero es posible que tenga que conocer el formato de píxel si está trabajando directamente con un mapa de bits en memoria o si combina Direct2D con Direct3D o GDI.

La [**enumeración DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) define una lista de formatos de píxel. La lista es bastante larga, pero solo algunas de ellas son relevantes para Direct2D. (Direct3D usa los demás).



| Formato de píxel                                                                                                                           | Descripción                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**<br/> | Este es el formato de píxel más común. Todos los componentes de píxeles (rojo, verde, azul y alfa) son enteros de 8 bits sin signo. Los componentes se organizan en *orden BGRA* en memoria. (Vea la ilustración siguiente).<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM**<br/> | Los componentes de píxel son enteros de 8 bits sin signo, *en orden RGBA.* En otras palabras, se intercambian los componentes rojo y azul, en relación con **DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**. Este formato solo se admite para dispositivos de hardware.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**DXGI \_ FORMAT \_ A8 \_ UNORM**<br/>                   | Este formato contiene un componente alfa de 8 bits, sin componentes RGB. Resulta útil para crear máscaras de opacidad. Para obtener más información sobre el uso de máscaras de opacidad en Direct2D, vea Información general sobre destinos [de representación A8 compatibles.](/windows/desktop/Direct2D/compatible-a8-rendertargets)<br/> |



 

En la ilustración siguiente se muestra el diseño de píxeles de BGRA.

![diagrama que muestra el diseño de píxeles bgra.](images/graphics14.png)

Para obtener el formato de píxel de un destino de representación, llame a [**ID2D1RenderTarget::GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). Es posible que el formato de píxel no coincida con la resolución de pantalla. Por ejemplo, la pantalla podría establecerse en un color de 16 bits, aunque el destino de representación use un color de 32 bits.

### <a name="alpha-mode"></a>Modo alfa

Un destino de representación también tiene un modo alfa, que define cómo se tratan los valores alfa.



| Modo alfa                           | Descripción                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OMITIR EL MODO ALFA D2D1 \_ \_ \_**        | No se realiza ninguna combinación alfa. Se omiten los valores alfa.                                                                                                                                                                                                                                                                          |
| **MODO ALFA D2D1 \_ \_ \_ DIRECTO**      | Alfa recta. Los componentes de color del píxel representan la intensidad del color antes de la mezcla alfa.                                                                                                                                                                                                                           |
| **MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO** | Alfa premultiplicado. Los componentes de color del píxel representan la intensidad del color multiplicada por el valor alfa. Este formato es más eficaz de representar que el alfa recta, porque el término (af Cf) de la fórmula de mezcla alfa está calculado previamente. Sin embargo, este formato no es adecuado para almacenar en un archivo de imagen. |



 

Este es un ejemplo de la diferencia entre alfa recta y alfa premultiplicado. Supongamos que el color deseado es rojo puro (100 % de intensidad) con un 50 % alfa. Como tipo Direct2D, este color se representaría como (1, 0, 0, 0,5). Con alfa recta y suponiendo componentes de color de 8 bits, el componente rojo del píxel se 0xFF. Con alfa premultiplicado, el componente rojo se escala en un 50 % para igualar 0x80.

El [**tipo de datos D2D1 COLOR \_ \_ F**](/windows/desktop/Direct2D/d2d1-color-f) siempre representa los colores mediante alfa recta. Direct2D convierte píxeles en formato alfa premultiplicado si es necesario.

Si sabe que el programa no realizará ninguna combinación alfa, cree el destino de representación con el modo alfa IGNORE del modo **ALFA \_ \_ \_ D2D1.** Este modo puede mejorar el rendimiento, ya que Direct2D puede omitir los cálculos alfa. Para obtener más información, [vea Improving the Performance of Direct2D Applications](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Siguientes

[Aplicación de transformaciones en Direct2D](applying-transforms-in-direct2d.md)

 

