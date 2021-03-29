---
title: Usar el color en Direct2D
description: Usar el color en Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358870"
---
# <a name="using-color-in-direct2d"></a>Usar el color en Direct2D

Direct2D usa el modelo de color RGB, en el que los colores se forman combinando valores diferentes de rojo, verde y azul. Un cuarto componente, alfa, mide la transparencia de un píxel. En Direct2D, cada uno de estos componentes es un valor de punto flotante con un intervalo de \[ 0,0 1,0 \] . En el caso de los tres componentes de color, el valor mide la intensidad del color. En el caso del componente alfa, 0,0 significa completamente transparente y 1,0 significa completamente opaco. En la tabla siguiente se muestran los colores resultantes de diversas combinaciones de intensidad del 100%.



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



 

![imagen que muestra los colores RGB.](images/graphics13.png)

Los valores de color entre 0 y 1 dan como resultado sombras diferentes de estos colores puros. Direct2D usa la estructura de [**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) para representar los colores. Por ejemplo, el código siguiente especifica magenta.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



También puede especificar un color mediante la clase [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) , que se deriva de la estructura [**\_ \_ F de color D2D1**](/windows/desktop/Direct2D/d2d1-color-f) .


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Combinación alfa

La combinación alfa crea áreas translúcidas mezclando el color de primer plano con el color de fondo mediante la siguiente fórmula.

<dl> color = AF * CF + (1-AF) * CB  
</dl>

donde *CB* es el color de fondo, *CF* es el color de primer plano y *AF* es el valor alfa del color de primer plano. Esta fórmula se aplica en pares a cada componente de color. Por ejemplo, supongamos que el color de primer plano es **(R = 1,0, G = 0,4, B = 0,0)**, con **alfa = 0,6** y el color de fondo es **(R = 0,0, G = 0,5, B = 1,0)**. El color de mezcla alfa resultante es:

R = (1,0 * 0,6 + 0 * 0,4) =. 6   
G = (0,4 * 0,6 + 0,5 * 0,4) =. 44  
B = (0 * 0,6 + 1,0 * 0,4) =. 40  

En la imagen siguiente se muestra el resultado de esta operación de mezcla.

![imagen que muestra la combinación alfa.](images/graphics15.png)

## <a name="pixel-formats"></a>Formatos de píxeles

La estructura [**D2D1 de \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) no describe cómo se representa un píxel en la memoria. En la mayoría de los casos, esto no importa. Direct2D controla todos los detalles internos de la traducción de la información de color en píxeles. Pero es posible que necesite conocer el formato de píxel si está trabajando directamente con un mapa de bits en la memoria o si combina Direct2D con Direct3D o GDI.

La enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) define una lista de formatos de píxeles. La lista es bastante larga, pero solo algunas de ellas son relevantes para Direct2D. (Direct3D usa los demás).



| Formato de píxeles                                                                                                                           | Descripción                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM**<br/> | Este es el formato de píxel más común. Todos los componentes de píxel (rojo, verde, azul y alfa) son enteros de 8 bits sin signo. Los componentes están organizados en orden *BGRA* en memoria. (Vea la ilustración siguiente).<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM**<br/> | Los componentes de píxeles son enteros de 8 bits sin signo, en orden *RGBA* . En otras palabras, los componentes rojo y azul se intercambian, con respecto al **formato de DXGI \_ \_ B8G8R8A8 \_ UNORM**. Este formato solo es compatible con dispositivos de hardware.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**Formato de DXGI \_ \_ a8 \_ UNORM**<br/>                   | Este formato contiene un componente alfa de 8 bits, sin componentes RGB. Resulta útil para crear máscaras de opacidad. Para obtener más información sobre el uso de las máscaras de opacidad en Direct2D, consulte [información general de destinos de representación de A8 compatibles](/windows/desktop/Direct2D/compatible-a8-rendertargets).<br/> |



 

En la ilustración siguiente se muestra el diseño de píxeles de BGRA.

![diagrama que muestra el diseño de píxeles de BGRA.](images/graphics14.png)

Para obtener el formato de píxel de un destino de representación, llame a [**ID2D1RenderTarget:: GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). El formato de píxel podría no coincidir con la resolución de pantalla. Por ejemplo, la pantalla se puede establecer en color de 16 bits, aunque el destino de representación usa el color de 32 bits.

### <a name="alpha-mode"></a>Modo alfa

Un destino de representación también tiene un modo alfa, que define cómo se tratan los valores alfa.



| Modo alfa                           | Descripción                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D2D1 \_ \_ modo alfa \_ omitir**        | No se realiza ninguna combinación alfa. Se omiten los valores alfa.                                                                                                                                                                                                                                                                          |
| **D2D1 \_ \_ modo alfa \_ recto**      | Alfa recto. Los componentes de color del píxel representan la intensidad de color antes de la combinación alfa.                                                                                                                                                                                                                           |
| **D2D1 \_ de \_ modo alfa \_ premultiplicado** | Alfa premultiplicado. Los componentes de color del píxel representan la intensidad de color multiplicada por el valor alfa. Este formato es más eficaz para representarse que el alfa recto, porque el término (AF CF) de la fórmula de combinación alfa se calcula previamente. Sin embargo, este formato no es adecuado para almacenar en un archivo de imagen. |



 

Este es un ejemplo de la diferencia entre alfa recto y alfa premultiplicado. Supongamos que el color deseado es rojo puro (intensidad del 100%) con 50% alfa. Como tipo de Direct2D, este color se representaría como (1, 0, 0, 0,5). Con Alpha recto y suponiendo que los componentes de color de 8 bits, el componente rojo del píxel es 0xFF. Mediante el uso de alfa premultiplicado, el componente rojo se escala en un 50% a un valor igual a 0x80.

El tipo de datos [**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) siempre representa los colores mediante alfa recto. Direct2D convierte los píxeles al formato alfa premultiplicado si es necesario.

Si sabe que el programa no realizará ninguna combinación alfa, cree el destino de representación con el modo **alfa de D2D1 \_ \_ \_ omitir** el modo alfa. Este modo puede mejorar el rendimiento, ya que Direct2D puede omitir los cálculos alfa. Para obtener más información, vea [mejorar el rendimiento de las aplicaciones de Direct2D](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Siguientes

[Aplicación de transformaciones en Direct2D](applying-transforms-in-direct2d.md)

 

