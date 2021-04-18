---
title: Funciones de transformación de vector 3D de DirectXMath
description: Muestra las funciones de transformación vector 3D.
ms.assetid: 148972da-e460-63b9-6b01-10201f63d157
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a592071970d69d7ef4b4db42960335c5fc771ac3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715596"
---
# <a name="directxmath-3d-vector-transformation-functions"></a><span data-ttu-id="620ed-103">Funciones de transformación de vector 3D de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="620ed-103">DirectXMath 3D vector transformation functions</span></span>

<span data-ttu-id="620ed-104">Muestra las funciones de transformación vector 3D.</span><span class="sxs-lookup"><span data-stu-id="620ed-104">Lists the 3D vector transformation functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="620ed-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="620ed-105">In this section</span></span>



| <span data-ttu-id="620ed-106">Tema</span><span class="sxs-lookup"><span data-stu-id="620ed-106">Topic</span></span>                                                                               | <span data-ttu-id="620ed-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="620ed-107">Description</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="620ed-108">**XMVector3InverseRotate**</span><span class="sxs-lookup"><span data-stu-id="620ed-108">**XMVector3InverseRotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3inverserotate)<br/>                 | <span data-ttu-id="620ed-109">Gira un vector 3D con el inverso de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="620ed-109">Rotates a 3D vector using the inverse of a quaternion.</span></span><br/>                                                                                |
| [<span data-ttu-id="620ed-110">**XMVector3Project**</span><span class="sxs-lookup"><span data-stu-id="620ed-110">**XMVector3Project**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)<br/>                             | <span data-ttu-id="620ed-111">Proyectar un vector 3D desde el espacio de objeto en el espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="620ed-111">Project a 3D vector from object space into screen space.</span></span><br/>                                                                              |
| [<span data-ttu-id="620ed-112">**XMVector3ProjectStream**</span><span class="sxs-lookup"><span data-stu-id="620ed-112">**XMVector3ProjectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)<br/>                 | <span data-ttu-id="620ed-113">Proyecta un flujo de vectores 3D del espacio de objeto en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="620ed-113">Projects a stream of 3D vectors from object space into screen space.</span></span><br/>                                                                  |
| [<span data-ttu-id="620ed-114">**XMVector3Rotate**</span><span class="sxs-lookup"><span data-stu-id="620ed-114">**XMVector3Rotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3rotate)<br/>                               | <span data-ttu-id="620ed-115">Gira un vector 3D con un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="620ed-115">Rotates a 3D vector using a quaternion.</span></span><br/>                                                                                               |
| [<span data-ttu-id="620ed-116">**XMVector3Transform**</span><span class="sxs-lookup"><span data-stu-id="620ed-116">**XMVector3Transform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)<br/>                         | <span data-ttu-id="620ed-117">Transforma un vector 3D mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="620ed-117">Transforms a 3D vector by a matrix.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="620ed-118">**XMVector3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="620ed-118">**XMVector3TransformCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)<br/>               | <span data-ttu-id="620ed-119">Transforma un vector 3D por una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="620ed-119">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span><br/>                                                      |
| [<span data-ttu-id="620ed-120">**XMVector3TransformCoordStream**</span><span class="sxs-lookup"><span data-stu-id="620ed-120">**XMVector3TransformCoordStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)<br/>   | <span data-ttu-id="620ed-121">Transforma un flujo de vectores 3D por una matriz determinada, proyectando los vectores resultantes de forma que sus coordenadas w sean iguales a 1,0.</span><span class="sxs-lookup"><span data-stu-id="620ed-121">Transforms a stream of 3D vectors by a given matrix, projecting the resulting vectors such that their w coordinates are equal to 1.0.</span></span><br/> |
| [<span data-ttu-id="620ed-122">**XMVector3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="620ed-122">**XMVector3TransformNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)<br/>             | <span data-ttu-id="620ed-123">Transforma el vector 3D normal de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="620ed-123">Transforms the 3D vector normal by the given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="620ed-124">**XMVector3TransformNormalStream**</span><span class="sxs-lookup"><span data-stu-id="620ed-124">**XMVector3TransformNormalStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)<br/> | <span data-ttu-id="620ed-125">Transforma una secuencia de vectores normales 3D por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="620ed-125">Transforms a stream of 3D normal vectors by a given matrix.</span></span><br/>                                                                           |
| [<span data-ttu-id="620ed-126">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="620ed-126">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)<br/>             | <span data-ttu-id="620ed-127">Transforma una secuencia de vectores 3D por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="620ed-127">Transforms a stream of 3D vectors by a given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="620ed-128">**XMVector3Unproject**</span><span class="sxs-lookup"><span data-stu-id="620ed-128">**XMVector3Unproject**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)<br/>                         | <span data-ttu-id="620ed-129">Proyecta un vector 3D a partir del espacio de la pantalla en el espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="620ed-129">Projects a 3D vector from screen space into object space.</span></span><br/>                                                                             |
| [<span data-ttu-id="620ed-130">**XMVector3UnprojectStream**</span><span class="sxs-lookup"><span data-stu-id="620ed-130">**XMVector3UnprojectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)<br/>             | <span data-ttu-id="620ed-131">Transforma un flujo de vectores 3D del espacio de pantalla al espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="620ed-131">Transforms a stream of 3D vectors from screen space to object space.</span></span><br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="620ed-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="620ed-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="620ed-133">Funciones de vector 3D de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="620ed-133">DirectXMath Library 3D Vector Functions</span></span>](ovw-xnamath-reference-functions-vector3.md)
</dt> </dl>

 

 
