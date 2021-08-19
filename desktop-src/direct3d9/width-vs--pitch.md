---
description: Aunque los términos ancho y tono se usan a menudo de forma informal, tienen significados muy importantes y claramente diferentes. Como resultado, debe comprender los significados de cada uno de ellos y cómo interpretar los valores que usa Direct3D para describirlos.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Ancho frente a tono (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1c697ec4c9278a78a5539818b30038d99fc9d59d96af7f22ee87c33949abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095524"
---
# <a name="width-vs-pitch-direct3d-9"></a>Ancho frente a tono (Direct3D 9)

Aunque los términos ancho y tono se usan a menudo de forma informal, tienen significados muy importantes y claramente diferentes. Como resultado, debe comprender los significados de cada uno de ellos y cómo interpretar los valores que usa Direct3D para describirlos.

Direct3D usa la [**estructura D3DSURFACE \_ DESC**](d3dsurface-desc.md) para llevar información que describe una superficie. Entre otras cosas, esta estructura se define para contener información sobre las dimensiones de una superficie, así como cómo esas dimensiones se representan en la memoria. La estructura usa los miembros Height y Width para describir las dimensiones lógicas de la superficie. Ambos miembros se miden en píxeles. Por lo tanto, los valores alto y ancho de una superficie de 640 x 480 son los mismos si se trata de una superficie de 8 bits o una superficie RGB de 24 bits.

Cuando se bloquea una superficie mediante el método [**IDirect3DSurface9::LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) el método rellena una estructura [**\_ RECT D3DLOCKED**](d3dlocked-rect.md) que contiene el tono de la superficie y un puntero a los bits bloqueados. El valor del miembro Pitch describe el tono de memoria de la superficie, también denominado stride. Pitch es la distancia, en bytes, entre dos direcciones de memoria que representan el principio de una línea de mapa de bits y el principio de la siguiente línea de mapa de bits. Dado que el tono se mide en bytes en lugar de píxeles, una superficie de 640 x 480x8 tiene un valor de paso muy diferente que una superficie con las mismas dimensiones, pero un formato de píxel diferente. Además, el valor de paso a veces refleja los bytes que Direct3D ha reservado como caché, por lo que no es seguro suponer que el tono es simplemente el ancho multiplicado por el número de bytes por píxel. En su lugar, visualice la diferencia entre el ancho y el tono, como se muestra en el diagrama siguiente.

![diagrama del tono y el ancho del mismo búfer frontal, búfer de reserva y caché](images/pitch.png)

En este diagrama, el búfer front-and-back son 640x480x8 y la caché es 384x480x8.

Al acceder directamente a las superficies, debe tener cuidado de permanecer dentro de la memoria asignada para las dimensiones de la superficie y no tener memoria reservada para la memoria caché. Además, al bloquear solo una parte de una superficie, debe permanecer dentro del rectángulo que especifique al bloquear la superficie. Si no se siguen estas directrices, se tendrán resultados impredecibles. Al representar directamente en la memoria de la superficie, use siempre el tono devuelto por el [**método IDirect3DSurface9::LockRect.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) No asuma un lanzamiento basado únicamente en el modo de presentación. Si la aplicación funciona en algunos adaptadores de pantalla pero parece desalineado en otros, esta puede ser la causa del problema.

Para obtener más información, vea [Accessing Surface Memory Directly (Direct3D 9) (Acceso](accessing-surface-memory-directly.md)directo a la memoria de superficie [Direct3D 9]).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
