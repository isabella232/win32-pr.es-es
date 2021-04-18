---
description: En esta sección se muestra cómo agregar Marcos y animaciones a un cubo simple.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Agregar Marcos y animaciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714786"
---
# <a name="adding-frames-and-animations-direct3d-9"></a><span data-ttu-id="6949b-103">Agregar Marcos y animaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6949b-103">Adding Frames and Animations (Direct3D 9)</span></span>

<span data-ttu-id="6949b-104">En esta sección se muestra cómo agregar Marcos y animaciones a un cubo simple.</span><span class="sxs-lookup"><span data-stu-id="6949b-104">This section shows how to add frames and animations to a simple cube.</span></span>

## <a name="working-with-frames"></a><span data-ttu-id="6949b-105">Trabajar con marcos</span><span class="sxs-lookup"><span data-stu-id="6949b-105">Working with Frames</span></span>

<span data-ttu-id="6949b-106">Se espera que un marco tome la siguiente estructura.</span><span class="sxs-lookup"><span data-stu-id="6949b-106">A frame is expected to take the following structure.</span></span>


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



<span data-ttu-id="6949b-107">Coloque la malla del cubo definida dentro de un marco con una transformación de identidad.</span><span class="sxs-lookup"><span data-stu-id="6949b-107">Place the defined cube mesh inside a frame with an identity transform.</span></span> <span data-ttu-id="6949b-108">A continuación, aplique una animación a este marco.</span><span class="sxs-lookup"><span data-stu-id="6949b-108">Then apply an animation to this frame.</span></span>


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



## <a name="working-with-animations"></a><span data-ttu-id="6949b-109">Trabajar con animaciones</span><span class="sxs-lookup"><span data-stu-id="6949b-109">Working with Animations</span></span>

<span data-ttu-id="6949b-110">Una animación se define mediante un conjunto de claves.</span><span class="sxs-lookup"><span data-stu-id="6949b-110">An animation is defined by a set of keys.</span></span> <span data-ttu-id="6949b-111">Una clave es un valor de hora asociado a una operación de escalado, una orientación o una posición.</span><span class="sxs-lookup"><span data-stu-id="6949b-111">A key is a time value associated with a scaling operation, an orientation, or a position.</span></span>


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



<span data-ttu-id="6949b-112">Las animaciones se agrupan en AnimationSets:</span><span class="sxs-lookup"><span data-stu-id="6949b-112">Animations are then grouped into AnimationSets:</span></span>


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



<span data-ttu-id="6949b-113">Ahora lleve el cubo a través de una animación.</span><span class="sxs-lookup"><span data-stu-id="6949b-113">Now take the cube through an animation.</span></span>


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



<span data-ttu-id="6949b-114">Para obtener más información, vea las plantillas [**Animation**](animation.md) y [**AnimationSet**](animationset.md) .</span><span class="sxs-lookup"><span data-stu-id="6949b-114">For more information, see the [**Animation**](animation.md) and [**AnimationSet**](animationset.md) templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6949b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6949b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6949b-116">Archivos X (heredado)</span><span class="sxs-lookup"><span data-stu-id="6949b-116">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



