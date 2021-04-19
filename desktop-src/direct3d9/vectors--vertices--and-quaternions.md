---
description: En Direct3D, los vértices describen la posición y la orientación. Cada vértice de una primitiva se describe mediante un vector que proporciona su posición, color, coordenadas de textura y un vector normal que proporciona su orientación.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vectores, vértices y cuaterniones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537024"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="6322b-104">Vectores, vértices y cuaterniones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6322b-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="6322b-105">En Direct3D, los vértices describen la posición y la orientación.</span><span class="sxs-lookup"><span data-stu-id="6322b-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="6322b-106">Cada vértice de una primitiva se describe mediante un vector que proporciona su posición, color, coordenadas de textura y un vector normal que proporciona su orientación.</span><span class="sxs-lookup"><span data-stu-id="6322b-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="6322b-107">Los cuaterniones agregan un cuarto elemento a los \[ valores x, y, z \] que definen un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="6322b-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="6322b-108">Los cuaterniones son una alternativa a los métodos de matriz que se usan normalmente para las rotaciones 3D.</span><span class="sxs-lookup"><span data-stu-id="6322b-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="6322b-109">Un cuaternión representa un eje en el espacio 3D y un giro alrededor de ese eje.</span><span class="sxs-lookup"><span data-stu-id="6322b-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="6322b-110">Por ejemplo, un cuaternión podría representar un eje (1,2) y un giro de 1 radianes.</span><span class="sxs-lookup"><span data-stu-id="6322b-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="6322b-111">Los cuaterniones incluyen información valiosa, pero su verdadera potencia procede de las dos operaciones que puede realizar en ellas: composición y interpolación.</span><span class="sxs-lookup"><span data-stu-id="6322b-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="6322b-112">La composición de los cuaterniones es similar a la combinación.</span><span class="sxs-lookup"><span data-stu-id="6322b-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="6322b-113">La composición de dos cuaterniones se expresa como la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="6322b-113">The composition of two quaternions is notated like the following illustration.</span></span>

![Ilustración de la notación cuaternión](images/quateq.png)

<span data-ttu-id="6322b-115">La composición de dos cuaterniones aplicados a una geometría significa "girar la geometría alrededor del eje ₂ por rotación ₂ y, a continuación, girarla alrededor del eje ₁ por rotación ₁".</span><span class="sxs-lookup"><span data-stu-id="6322b-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="6322b-116">En este caso, Q representa una rotación alrededor de un eje único que es el resultado de aplicar q ₂ y, a continuación, de q ₁ a Geometry.</span><span class="sxs-lookup"><span data-stu-id="6322b-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="6322b-117">Mediante la interpolación cuaternión, una aplicación puede calcular una ruta de acceso fluida y razonable de un eje y la orientación a otra.</span><span class="sxs-lookup"><span data-stu-id="6322b-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="6322b-118">Por lo tanto, la interpolación entre q ₁ y q ₂ proporciona una manera sencilla de animar de una orientación a otra.</span><span class="sxs-lookup"><span data-stu-id="6322b-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="6322b-119">Al usar la composición y la interpolación juntas, proporcionan una manera sencilla de manipular una geometría de una manera que parezca compleja.</span><span class="sxs-lookup"><span data-stu-id="6322b-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="6322b-120">Por ejemplo, Imagine que tiene una geometría que desea rotar a una orientación determinada.</span><span class="sxs-lookup"><span data-stu-id="6322b-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="6322b-121">Ya sabe que desea rotar ₂ grados en torno a ₂ de eje y, a continuación, girarlo r ₁ degrees alrededor de la ₁ de eje, pero no conoce el cuaternión final.</span><span class="sxs-lookup"><span data-stu-id="6322b-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="6322b-122">Mediante el uso de composición, se pueden combinar las dos rotaciones en la geometría para obtener un único cuaternión que sea el resultado.</span><span class="sxs-lookup"><span data-stu-id="6322b-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="6322b-123">A continuación, se podría interpolar desde el cuaternión original con el cuaternión compuesto para lograr una transición suave de uno a otro.</span><span class="sxs-lookup"><span data-stu-id="6322b-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="6322b-124">La biblioteca de utilidades de D3DX incluye funciones que le ayudan a trabajar con cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="6322b-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="6322b-125">Por ejemplo, la función [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) agrega un valor de giro a un vector que define un eje de rotación y devuelve el resultado en un cuaternión definido por una estructura [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="6322b-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="6322b-126">Además, la función [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) crea cuaterniones y [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) realiza la interpolación lineal esférica entre dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="6322b-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="6322b-127">Las aplicaciones Direct3D pueden utilizar las siguientes funciones para simplificar la tarea de trabajar con cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="6322b-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="6322b-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="6322b-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="6322b-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="6322b-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="6322b-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="6322b-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="6322b-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="6322b-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="6322b-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="6322b-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="6322b-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="6322b-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="6322b-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="6322b-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="6322b-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="6322b-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="6322b-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="6322b-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="6322b-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="6322b-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="6322b-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="6322b-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="6322b-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="6322b-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="6322b-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="6322b-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="6322b-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="6322b-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="6322b-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="6322b-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="6322b-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="6322b-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="6322b-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="6322b-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="6322b-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="6322b-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="6322b-146">Las aplicaciones Direct3D pueden utilizar las siguientes funciones para simplificar la tarea de trabajar con vectores de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="6322b-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="6322b-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="6322b-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="6322b-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="6322b-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="6322b-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="6322b-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="6322b-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="6322b-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="6322b-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="6322b-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="6322b-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="6322b-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="6322b-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="6322b-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="6322b-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="6322b-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="6322b-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="6322b-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="6322b-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="6322b-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="6322b-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="6322b-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="6322b-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="6322b-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="6322b-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="6322b-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="6322b-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="6322b-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="6322b-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="6322b-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="6322b-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="6322b-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="6322b-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="6322b-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="6322b-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="6322b-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="6322b-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="6322b-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="6322b-166">Se incluyen muchas funciones adicionales que simplifican las tareas con dos y cuatro vectores de componentes entre las [funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md) suministradas por la biblioteca de utilidades de D3DX.</span><span class="sxs-lookup"><span data-stu-id="6322b-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6322b-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6322b-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6322b-168">Sistemas de coordenadas y geometría</span><span class="sxs-lookup"><span data-stu-id="6322b-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



