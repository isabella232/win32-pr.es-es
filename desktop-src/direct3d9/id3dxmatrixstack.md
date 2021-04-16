---
description: Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matriz.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interfaz ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708071"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="0c673-103">Interfaz ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="0c673-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="0c673-104">Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matriz.</span><span class="sxs-lookup"><span data-stu-id="0c673-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="0c673-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c673-105">Members</span></span>

<span data-ttu-id="0c673-106">La interfaz **ID3DXMATRIXStack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0c673-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0c673-107">**ID3DXMATRIXStack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c673-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="0c673-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c673-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0c673-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c673-109">Methods</span></span>

<span data-ttu-id="0c673-110">La interfaz **ID3DXMATRIXStack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0c673-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="0c673-111">Método</span><span class="sxs-lookup"><span data-stu-id="0c673-111">Method</span></span>                                                                       | <span data-ttu-id="0c673-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c673-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c673-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="0c673-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="0c673-114">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="0c673-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="0c673-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="0c673-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="0c673-116">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="0c673-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0c673-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="0c673-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="0c673-118">Carga la matriz especificada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="0c673-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="0c673-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="0c673-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="0c673-120">Determina el producto de la matriz actual y la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="0c673-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="0c673-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="0c673-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="0c673-122">Determina el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="0c673-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="0c673-123">**Emergente**</span><span class="sxs-lookup"><span data-stu-id="0c673-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="0c673-124">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="0c673-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="0c673-125">**Inserción**</span><span class="sxs-lookup"><span data-stu-id="0c673-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="0c673-126">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="0c673-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="0c673-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="0c673-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="0c673-128">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0c673-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="0c673-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="0c673-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="0c673-130">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0c673-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="0c673-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="0c673-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="0c673-132">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0c673-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="0c673-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="0c673-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="0c673-134">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0c673-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="0c673-135">**Escala**</span><span class="sxs-lookup"><span data-stu-id="0c673-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="0c673-136">Escalar la matriz actual sobre el origen de la coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="0c673-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="0c673-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="0c673-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="0c673-138">Escala la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c673-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="0c673-139">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="0c673-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="0c673-140">Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="0c673-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="0c673-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="0c673-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="0c673-142">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="0c673-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c673-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c673-143">Remarks</span></span>

<span data-ttu-id="0c673-144">La interfaz **ID3DXMATRIXStack** se obtiene mediante una llamada a la función [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="0c673-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="0c673-145">El tipo LPD3DXMATRIXSTACK se define como un puntero a la interfaz **ID3DXMATRIXStack** .</span><span class="sxs-lookup"><span data-stu-id="0c673-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="0c673-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c673-146">Requirements</span></span>



| <span data-ttu-id="0c673-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c673-147">Requirement</span></span> | <span data-ttu-id="0c673-148">Value</span><span class="sxs-lookup"><span data-stu-id="0c673-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c673-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c673-149">Header</span></span><br/>  | <dl> <span data-ttu-id="0c673-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c673-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0c673-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c673-151">Library</span></span><br/> | <dl> <span data-ttu-id="0c673-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c673-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c673-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c673-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c673-154">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="0c673-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
