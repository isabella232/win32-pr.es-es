---
description: Aunque el ancho y el paso de los términos se usan a menudo de manera informativa, tienen significados muy importantes y claramente distintos. Como resultado, debe comprender los significados de cada uno de ellos y cómo interpretar los valores que usa Direct3D para describirlos.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Ancho frente a paso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566154"
---
# <a name="width-vs-pitch-direct3d-9"></a>Ancho frente a paso (Direct3D 9)

Aunque el ancho y el paso de los términos se usan a menudo de manera informativa, tienen significados muy importantes y claramente distintos. Como resultado, debe comprender los significados de cada uno de ellos y cómo interpretar los valores que usa Direct3D para describirlos.

Direct3D usa la estructura [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) para llevar información que describe una superficie. Entre otras cosas, esta estructura se define para contener información sobre las dimensiones de una superficie, así como el modo en que esas dimensiones se representan en la memoria. La estructura usa los miembros height y Width para describir las dimensiones lógicas de la superficie. Ambos miembros se miden en píxeles. Por lo tanto, los valores de alto y ancho de una superficie 640 x 480 son los mismos que si se trata de una superficie de 8 bits o una superficie RGB de 24 bits.

Cuando se bloquea una superficie mediante el método [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , el método rellena una estructura [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) que contiene el tono de la superficie y un puntero a los bits bloqueados. El valor del miembro de paso describe el paso de memoria de la superficie, también denominado STRIDE. El paso es la distancia, en bytes, entre dos direcciones de memoria que representan el principio de una línea de mapa de bits y el principio de la siguiente línea de mapa de bits. Dado que el paso se mide en bytes en lugar de en píxeles, una superficie 640x480x8 tiene un valor de tono muy diferente que una superficie con las mismas dimensiones pero un formato de píxel diferente. Además, el valor de paso refleja a veces los bytes que Direct3D ha reservado como caché, por lo que no es seguro suponer que el paso es simplemente el ancho multiplicado por el número de bytes por píxel. En su lugar, visualice la diferencia entre el ancho y el tono tal y como se muestra en el diagrama siguiente.

![diagrama del tono y el ancho del mismo búfer frontal, búfer de reserva y caché](images/pitch.png)

En este diagrama, el búfer frontal y el búfer de reserva son ambos 640x480x8 y la memoria caché es 384x480x8.

Al acceder directamente a las superficies, tenga cuidado de permanecer dentro de la memoria asignada para las dimensiones de la superficie y dejar fuera de la memoria reservada para la memoria caché. Además, al bloquear solo una parte de una superficie, debe permanecer dentro del rectángulo que especifique al bloquear la superficie. Si no se siguen estas instrucciones, se obtendrán resultados imprevisibles. Al representar directamente en la memoria de superficie, use siempre el paso devuelto por el método [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) . No asuma un tono basado únicamente en el modo de presentación. Si la aplicación funciona en algunos adaptadores de pantalla, pero parece ilegible en otros, puede ser la causa del problema.

Para obtener más información, vea [acceso directo a la memoria de la superficie (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
