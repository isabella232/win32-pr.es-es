---
description: En esta sección se presentan los conceptos básicos de la transformación vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Transformación de vista (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537582"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="ff79c-103">Transformación de vista (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ff79c-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="ff79c-104">En esta sección se presentan los conceptos básicos de la transformación vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ff79c-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="ff79c-105">La transformación de vista busca el visor en el espacio universal, transformando los vértices en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="ff79c-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="ff79c-106">En el espacio de la cámara, la cámara o el visor, está en el origen y busca en la dirección z positiva.</span><span class="sxs-lookup"><span data-stu-id="ff79c-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="ff79c-107">Recuerde que Direct3D usa un sistema de coordenadas a la izquierda, por lo que z es positivo en una escena.</span><span class="sxs-lookup"><span data-stu-id="ff79c-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="ff79c-108">La matriz de la vista reubica los objetos del mundo en torno a la posición de una cámara: el origen del espacio de la cámara y la orientación.</span><span class="sxs-lookup"><span data-stu-id="ff79c-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="ff79c-109">Hay muchas maneras de crear una matriz de vista.</span><span class="sxs-lookup"><span data-stu-id="ff79c-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="ff79c-110">En todos los casos, la cámara tiene una posición lógica y una orientación en el espacio universal que se usa como punto de partida para crear una matriz de vistas que se aplicará a los modelos de una escena.</span><span class="sxs-lookup"><span data-stu-id="ff79c-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="ff79c-111">La matriz de la vista traduce y gira los objetos para colocarlos en el espacio de la cámara, donde la cámara está en el origen.</span><span class="sxs-lookup"><span data-stu-id="ff79c-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="ff79c-112">Una manera de crear una matriz de vistas es combinar una matriz de traslación con matrices de rotación para cada eje.</span><span class="sxs-lookup"><span data-stu-id="ff79c-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="ff79c-113">En este enfoque, se aplica la siguiente ecuación de matriz general.</span><span class="sxs-lookup"><span data-stu-id="ff79c-113">In this approach, the following general matrix equation applies.</span></span>

![ecuación de la transformación de vista](images/viewtran.png)

<span data-ttu-id="ff79c-115">En esta fórmula, V es la matriz de vistas que se está creando, T es una matriz de traducción que recoloca objetos en el mundo y R ₓ a R<sub>z</sub> son matrices de rotación que giran objetos a lo largo de los ejes x-, y-y z.</span><span class="sxs-lookup"><span data-stu-id="ff79c-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="ff79c-116">Las matrices de traslación y rotación se basan en la posición lógica y la orientación de la cámara en el espacio universal.</span><span class="sxs-lookup"><span data-stu-id="ff79c-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="ff79c-117">Por lo tanto, si la posición lógica de la cámara en el mundo es <10, 20100>, el objetivo de la matriz de traslación es mover objetos-10 unidades a lo largo del eje x,-20 unidades a lo largo del eje y, y-100 unidades a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="ff79c-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="ff79c-118">Las matrices de rotación de la fórmula se basan en la orientación de la cámara, en cuanto a la cantidad de ancho de los ejes del espacio de la cámara que se giran con el espacio universal.</span><span class="sxs-lookup"><span data-stu-id="ff79c-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="ff79c-119">Por ejemplo, si la cámara mencionada anteriormente apunta hacia abajo, su eje z es 90 grados (pi/2 radianes) fuera de la alineación con el eje z del espacio universal, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ff79c-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![Ilustración del espacio de vista de la cámara en comparación con el espacio universal](images/camtop.png)

<span data-ttu-id="ff79c-121">Las matrices de rotación aplican rotaciones de la misma magnitud, pero opuestas, a los modelos de la escena.</span><span class="sxs-lookup"><span data-stu-id="ff79c-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="ff79c-122">La matriz de la vista de esta cámara incluye un giro de-90 grados alrededor del eje x.</span><span class="sxs-lookup"><span data-stu-id="ff79c-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="ff79c-123">La matriz de rotación se combina con la matriz de traslación para crear una matriz de vista que ajusta la posición y la orientación de los objetos de la escena para que su parte superior esté orientada a la cámara, lo que proporciona la apariencia de que la cámara está por encima del modelo.</span><span class="sxs-lookup"><span data-stu-id="ff79c-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="ff79c-124">Configurar una matriz de vistas</span><span class="sxs-lookup"><span data-stu-id="ff79c-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="ff79c-125">Las funciones auxiliares [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) y [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) crean una matriz de vista basada en la ubicación de la cámara y un punto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff79c-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="ff79c-126">En el ejemplo siguiente se crea una matriz de vista para las coordenadas de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="ff79c-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="ff79c-127">Direct3D usa el mundo y las matrices de vistas para configurar varias estructuras de datos internas.</span><span class="sxs-lookup"><span data-stu-id="ff79c-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="ff79c-128">Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas.</span><span class="sxs-lookup"><span data-stu-id="ff79c-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="ff79c-129">Establecer estas matrices con frecuencia es un proceso que consume mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="ff79c-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="ff79c-130">Puede minimizar el número de cálculos necesarios concatenando el mundo y ver las matrices en una matriz de vista mundial que establezca como la matriz universal y, a continuación, estableciendo la matriz de la vista en la identidad.</span><span class="sxs-lookup"><span data-stu-id="ff79c-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="ff79c-131">Mantenga copias en caché de matrices de mundo y vistas individuales que puede modificar, concatenar y restablecer la matriz universal según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ff79c-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="ff79c-132">Para mayor claridad, los ejemplos raramente emplean esta optimización.</span><span class="sxs-lookup"><span data-stu-id="ff79c-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff79c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff79c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff79c-134">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="ff79c-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



