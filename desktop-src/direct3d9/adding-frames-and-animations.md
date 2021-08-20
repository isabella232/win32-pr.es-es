---
description: En esta sección se muestra cómo agregar fotogramas y animaciones a un cubo simple.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Agregar fotogramas y animaciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbe0da64e5eabff72f0977a8a55f23d3e4756c7681aa2c806b6ee1d794362cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097197"
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

 

 



