---
description: Trabajar con RGB de 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Trabajar con RGB de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272607"
---
# <a name="working-with-16-bit-rgb"></a>Trabajar con RGB de 16 bits

Se definen dos formatos para RGB sin comprimir de 16 bits:

-   MEDIASUBTYPE \_ 555 usa cinco bits cada uno para los componentes rojo, verde y azul de un píxel. Se omite el bit más significativo de **WORD.**
-   MEDIASUBTYPE 565 usa cinco bits para los componentes rojo y azul, y \_ seis bits para el componente verde. Este formato refleja el hecho de que la visión humana es más sensible a las partes verdes del espectro visible.

**RGB 565**

Para extraer los componentes de color de una imagen RGB 565, trate cada píxel como un tipo **WORD** y use las siguientes máscaras de bits:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Obtenga los componentes de color de un píxel como se muestra a continuación:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Recuerde que los canales rojo y azul son de 5 bits y el canal verde es de 6 bits. Para convertir estos valores en componentes de 8 bits (para RGB de 24 o 32 bits), debe desplazar a la izquierda el número adecuado de bits:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Invierta este proceso para crear un RGB de 565 píxeles. Suponiendo que los valores de color se hayan truncado al número correcto de bits:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

Trabajar con RGB 555 es básicamente lo mismo que RGB 565, salvo que las operaciones de desplazamiento de bits y máscaras de bits son diferentes. Para obtener los componentes de color de un RGB de 555 píxeles, haga lo siguiente:


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Para empaquetar los valores de color rojo, verde y azul en un RGB de 555 píxeles, haga lo siguiente:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subtipos de vídeo RGB sin comprimir](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



