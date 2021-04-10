---
description: Los vértices del espacio de la cámara se calculan transformando los vértices del objeto con la matriz de la vista mundial.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformaciones del espacio de la cámara (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153129"
---
# <a name="camera-space-transformations-direct3d-9"></a>Transformaciones del espacio de la cámara (Direct3D 9)

Los vértices del espacio de la cámara se calculan transformando los vértices del objeto con la matriz de la vista mundial.

V = V \* wvMatrix

Las normales de vértice, en el espacio de la cámara, se calculan transformando las normales del objeto con la transformación inversa de la matriz de la vista mundial. La matriz de vista mundial puede o no ser ortogonal.

N = N \* (wvMatrix ⁻ ¹)<sup>T</sup>

La inversión de matriz y la conversión de matriz operan en una matriz de 4x4. La multiplicación combina el normal con la parte 3x3 de la matriz 4x4 resultante.

Si el estado de representación, D3DRENDERSTATE \_ NORMALIZENORMALS se establece en **true**, los vectores normales de vértices se normalizan después de la transformación en el espacio de la cámara como se indica a continuación:

N = norma (N)

La posición de la luz en el espacio de la cámara se calcula transformando la posición de la fuente de luz con la matriz de la vista.

LP = LP \* vMatrix

La dirección de la luz en el espacio de la cámara para una luz direccional se calcula multiplicando la dirección de origen de la luz por la matriz de la vista, normalizando y negando el resultado.

L<sub>dir</sub> =-norma (L<sub>dir</sub> \* wvMatrix)

En el caso del \_ punto D3DLIGHT y D3DLIGHT, \_ la dirección de la luz se calcula de la manera siguiente:

L<sub>dir</sub> = norma (V \* LP), donde los parámetros se definen en la tabla siguiente.



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <sub>Directorio</sub> L | N/D           | D3DVECTOR | Vector de dirección desde el vértice del objeto hasta la luz          |
| V               | N/D           | D3DVECTOR | Posición del vértice en el espacio de la cámara                           |
| wvMatrix        | Identidad      | D3DMATRIX | Matriz compuesta que contiene las transformaciones mundo y vista |
| N               | N/D           | D3DVECTOR | Vértice normal                                             |
| LP              | N/D           | D3DVECTOR | Posición clara en el espacio de la cámara                            |
| vMatrix         | Identidad      | D3DMATRIX | Matriz que contiene la transformación de la vista                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



