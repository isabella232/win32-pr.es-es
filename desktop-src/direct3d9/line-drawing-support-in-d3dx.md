---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a0fdeb24dad1107f85e6c79603368776bce15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422959"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

D3DX admite líneas con suavizado de ancho único de píxel. Ya no se admiten los patrones de línea.

La biblioteca de dibujos de líneas emula líneas mediante triángulos de textura y asume lo siguiente:

-   El hardware está disponible a través de las interfaces de Direct3D 9.
-   Al menos una fase de textura está disponible.
-   se usan las texturas de 64 x 64.
-   Están disponibles los siguientes modos:
    -   Filtrado bilineal
    -   Modo de dirección de abrazadera
    -   Modo de dirección de encapsulación
    -   Operación alfa modular
    -   Combinación alfa (SRCBLEND = SRC \_ Alpha, DESTBLEND = INV \_ src \_ Alpha)
    -   Prueba alfa si la combinación alfa no está disponible; resultado de menor calidad

En el caso de la representación de líneas alisadas en destinos de representación Multimuestra, use [**ID3DXLine**](id3dxline.md) , que genera polígonos con textura. Los valores de cobertura de píxeles, generados por la rasterización de líneas alisadas, modulan el valor alfa del píxel calculado por el sombreador de píxeles. Para dibujar una línea alisada, una aplicación debe habilitar la combinación alfa y, a continuación, debe establecer el \_ Estado de representación de D3DRS ANTIALIASEDLINEENABLE en **true**.

## <a name="functionality-description"></a>Descripción de la funcionalidad

La biblioteca admite el dibujo de franjas de líneas coloreadas con las siguientes características de línea, cada una de las cuales es independiente de cualquier otra:

-   Ancho de línea
-   Patrón de línea con repetición (el contador de patrón de línea se restablece con cada [**ID3DXLine::D RAW**](id3dxline--draw.md) o [**ID3DXLine::D rawtransform**](id3dxline--drawtransform.md) Call. No se restablece con cada segmento de la franja de líneas).
-   Suavizado
-   Líneas de estilo OpenGL

> [!Note]  
> No se admite ningún inglete.

 

La biblioteca usa la compatibilidad de dibujo de línea de hardware nativa (si está disponible en el dispositivo) solo si:

-   El ancho de línea es 1.
-   No se habilita ningún patrón de línea.

El hardware admite las líneas con suavizado de un solo píxel, por lo que la biblioteca lo usa, si está disponible. El miembro LineCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera las capacidades de hardware para los primitivos de dibujo de línea.

Cuando se usa el dibujo de línea de software, cada línea se expande en un rectángulo y se envían cuatro vértices al controlador.

Cada segmento de línea se dibuja con dos triángulos. El ancho de la primitiva es el ancho especificado más 1,0, lo que puede dar lugar a una fila o columna adicional de píxeles. A medida que la línea se hace más ancha, el degradado antialias en la textura se vuelve más grueso y se replican texturas más opacas en torno a la mitad. El degradado se codifica en la dirección v de la textura y normalmente se replica a lo largo de la dirección u. El modo de direccionamiento de textura para v es Clamp.

Cada segmento de línea de la lista se puede considerar una línea independiente que se inicia desde el punto final anterior.

La calidad de suavizado de contorno a lo largo de los bordes paralela a la longitud de la línea original se ve afectada a medida que la línea es más ancha. Se espera que el ancho de línea sea mayor que 32,0 empiece a mostrar artefactos a lo largo de estos bordes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



