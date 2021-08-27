---
description: Obtenga información sobre la compatibilidad con el dibujo de línea en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Compatibilidad con dibujo de líneas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cf107615410da6dcfba02d6f708129429e31586360183277fb8f669653d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799686"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Compatibilidad con dibujo de líneas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

D3DX admite líneas suavizadas de contorno de un solo píxel. Ya no se admiten los patrones de línea.

La biblioteca de dibujo de líneas emula líneas mediante triángulos de textura y asume lo siguiente:

-   El hardware está disponible a través de las interfaces de Direct3D 9.
-   Hay al menos una fase de textura disponible.
-   Se usan texturas de 64 x 64.
-   Están disponibles los siguientes modos:
    -   Filtrado bilineal
    -   Modo de dirección de fijación
    -   Modo de encapsulado de direcciones
    -   Modular de operación alfa
    -   Combinación alfa (SRCBLEND = SRC \_ ALPHA, DESTBLEND = INV \_ SRC \_ ALPHA)
    -   Prueba alfa si la combinación alfa no está disponible; resultado de menor calidad

Para la representación de líneas suavizadas en destinos de representación multimuestreo, use [**ID3DXLine,**](id3dxline.md) que genera polígonos con textura. Los valores de cobertura de píxeles, generados por la rasterización de línea con suavizado de contorno, modularan el valor alfa del píxel calculado por el sombreador de píxeles. Para dibujar una línea con suavizado de contorno, una aplicación debe habilitar la combinación alfa y, a continuación, debe establecer el estado de representación D3DRS \_ ANTIALIASEDLINEENABLE en **TRUE.**

## <a name="functionality-description"></a>Descripción de la funcionalidad

La biblioteca admite el dibujo de franjas de líneas de color con las siguientes características de línea, cada una de las cuales es independiente de cualquier otra:

-   Ancho de línea
-   Patrón de línea con repetición (el contador del patrón de línea se restablece con cada [**llamada ID3DXLine::D raw**](id3dxline--draw.md) o [**ID3DXLine::D rawTransform.**](id3dxline--drawtransform.md) No se restablece con cada segmento de la franja de línea).
-   Antialiasing
-   Líneas de estilo OpenGL

> [!Note]  
> No se admite la inglete.

 

La biblioteca usa compatibilidad nativa con dibujo de línea de hardware (si está disponible en el dispositivo) solo si:

-   El ancho de línea es 1.
-   No hay ningún patrón de línea habilitado.

Algunas líneas con suavizado de contorno de un solo píxel son compatibles con hardware, por lo que la biblioteca lo usa, si está disponible. El miembro LineCaps de la [**estructura D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera las funcionalidades de hardware para primitivos de dibujo de línea.

Cuando se usa el dibujo de línea de software, cada línea se expande en un rectángulo y se envían cuatro vértices al controlador.

Cada segmento de línea se dibuja con dos triángulos. El ancho de la primitiva es el ancho especificado más 1,0, lo que puede dar lugar a una fila o columna adicionales de píxeles. A medida que la línea se hace más ancha, el degradado de antialias de la textura se vuelve más general y los elementos de textura más opacos se replican alrededor del centro. El degradado se codifica en la dirección v de la textura y normalmente se replica a lo largo de la dirección U. El modo de direccionamiento de textura para v es la fijación.

Cada segmento de línea de la lista se puede considerar una línea independiente que comienza desde el punto de finalización anterior.

La calidad del suavizado de contorno a lo largo de los bordes paralelos a la longitud de la línea original se sufre a medida que la línea se hace más ancha. Se espera que los anchos de línea mayores que 32,0 empiecen a mostrar artefactos a lo largo de estos bordes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



