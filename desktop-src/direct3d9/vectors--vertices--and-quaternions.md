---
description: En Direct3D, los vértices describen la posición y la orientación. Cada vértice de una primitiva se describe mediante un vector que proporciona su posición, color, coordenadas de textura y un vector normal que proporciona su orientación.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vectores, vértices y cuaterniones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b6a71dcb00356d4de4637a6aabb1eba5c02e49c62380b32732351d15bfcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290451"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vectores, vértices y cuaterniones (Direct3D 9)

En Direct3D, los vértices describen la posición y la orientación. Cada vértice de una primitiva se describe mediante un vector que proporciona su posición, color, coordenadas de textura y un vector normal que proporciona su orientación.

Los cuaterniones agregan un cuarto elemento a los valores \[ x, y, z \] que definen un vector de tres componentes. Los cuaterniones son una alternativa a los métodos de matriz que normalmente se usan para las rotaciones 3D. Un cuaternión representa un eje en espacio 3D y una rotación alrededor de ese eje. Por ejemplo, un cuaternión podría representar un eje (1,1,2) y una rotación de 1 radián. Los cuaterniones llevan información valiosa, pero su verdadera potencia procede de las dos operaciones que se pueden realizar en ellas: composición e interpolación.

La composición en cuaterniones es similar a combinarlas. La composición de dos cuaterniones se anota como en la ilustración siguiente.

![ilustración de la notación de cuaternión](images/quateq.png)

La composición de dos cuaterniones aplicadas a una geometría significa "girar la geometría alrededor del eje 3 girando por rotación y, a continuación, girarla alrededor del eje₁ por rotación₁". En este caso, Q representa una rotación alrededor de un único eje que es el resultado de aplicar q3 y, a continuación, q₁ a la geometría.

Mediante la interpolación de cuaternión, una aplicación puede calcular una ruta de acceso suave y razonable de un eje y orientación a otro. Por lo tanto, la interpolación entre q₁ y q3 proporciona una manera sencilla de animar de una orientación a otra.

Cuando se usa la composición y la interpolación juntos, proporcionan una manera sencilla de manipular una geometría de una manera que parece compleja. Por ejemplo, imagine que tiene una geometría que desea girar a una orientación determinada. Sabe que quiere girarlo r3 grados alrededor del eje 3 y, a continuación₁ girarlo r₁ grados alrededor del eje₁ pero no conoce el cuaternión final. Mediante el uso de la composición, podría combinar las dos rotaciones en la geometría para obtener un cuaternión único que sea el resultado. A continuación, podría interpolar desde el cuaternión original al cuaternión compuesto para lograr una transición suave de una a otra.

La biblioteca de utilidades D3DX incluye funciones que le ayudan a trabajar con cuaterniones. Por ejemplo, la función [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) agrega un valor de rotación a un vector que define un eje de rotación y devuelve el resultado en un cuaternión definido por una estructura [**D3DXQUATERNION.**](d3dxquaternion.md) Además, la función [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compone cuaterniones y [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) realiza la interpolación lineal esférica entre dos cuaterniones.

Las aplicaciones de Direct3D pueden usar las siguientes funciones para simplificar la tarea de trabajar con cuaterniones.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Las aplicaciones de Direct3D pueden usar las siguientes funciones para simplificar la tarea de trabajar con vectores de tres componentes.

-   [**D3DXVec3Agregue**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

Muchas funciones adicionales que simplifican las tareas mediante vectores [](dx9-graphics-reference-d3dx-functions-math.md) de dos y cuatro componentes se incluyen entre las funciones matemáticas proporcionadas por la biblioteca de utilidades D3DX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



