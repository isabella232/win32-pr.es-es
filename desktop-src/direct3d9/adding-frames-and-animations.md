---
description: En esta sección se muestra cómo agregar fotogramas y animaciones a un cubo simple.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Agregar fotogramas y animaciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566161"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Agregar fotogramas y animaciones (Direct3D 9)

En esta sección se muestra cómo agregar fotogramas y animaciones a un cubo simple.

## <a name="working-with-frames"></a>Trabajar con fotogramas

Se espera que un marco tome la siguiente estructura.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Coloque la malla de cubo definida dentro de un marco con una transformación de identidad. A continuación, aplique una animación a este marco.


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>Trabajar con animaciones

Una animación se define mediante un conjunto de claves. Una clave es un valor de tiempo asociado a una operación de escalado, una orientación o una posición.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



A continuación, las animaciones se agrupan en AnimationSets:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



Ahora, lleve el cubo a través de una animación.


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



Para obtener más información, vea las [**plantillas Animation**](animation.md) [**y AnimationSet.**](animationset.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos X (heredados)](x-files--legacy-.md)
</dt> </dl>

 

 



