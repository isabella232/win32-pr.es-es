---
description: Los vértices del espacio de la cámara se calculan mediante la transformación de los vértices de objeto con la matriz de vistas del mundo.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformaciones de espacio de cámara (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568972"
---
# <a name="camera-space-transformations-direct3d-9"></a>Transformaciones de espacio de cámara (Direct3D 9)

Los vértices del espacio de la cámara se calculan mediante la transformación de los vértices de objeto con la matriz de vistas del mundo.

V = V \* wvMatrix

Las normales de vértice, en el espacio de la cámara, se calculan transformando los normales de objeto con la transpuesta inversa de la matriz de vista del mundo. La matriz de vistas del mundo puede o no ser ortogonal.

N = N \* (wvMatrix,¹)<sup>T</sup>

La inversión de matriz y la transpuesta de matriz funcionan en una matriz 4x4. La multiplicación combina lo normal con la parte 3x3 de la matriz 4x4 resultante.

Si el estado de representación, D3DRENDERSTATE NORMALIZENORMALS se establece en TRUE, los vectores normales de vértice se normalizan después de la transformación en el espacio de la cámara de la \_ siguiente manera: 

N = norm(N)

La posición de la luz en el espacio de la cámara se calcula transformando la posición de la fuente de luz con la matriz de vista.

Lp = Lp \* vMatrix

La dirección a la luz en el espacio de la cámara para una luz direccional se calcula multiplicando la dirección de la fuente de luz por la matriz de vista, normalizando y negando el resultado.

L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)

Para D3DLIGHT \_ POINT y D3DLIGHT SPOT, la dirección a la luz \_ se calcula de la siguiente manera:

L<sub>dir</sub> = norm(V \* Lp), donde los parámetros se definen en la tabla siguiente.



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vector de dirección desde el vértice del objeto a la luz          |
| V               | N/D           | D3DVECTOR | Posición del vértice en el espacio de la cámara                           |
| wvMatrix        | Identidad      | D3DMATRIX | Matriz compuesta que contiene el mundo y las transformaciones de vista |
| No               | N/D           | D3DVECTOR | Vértice normal                                             |
| Lp              | N/D           | D3DVECTOR | Posición ligera en el espacio de la cámara                            |
| vMatrix         | Identidad      | D3DMATRIX | Matriz que contiene la transformación de vista                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



