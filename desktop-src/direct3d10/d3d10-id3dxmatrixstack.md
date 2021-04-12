---
description: Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matriz.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interfaz ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362727"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="6233d-103">Interfaz ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="6233d-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="6233d-104">Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matriz.</span><span class="sxs-lookup"><span data-stu-id="6233d-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="6233d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6233d-105">Members</span></span>

<span data-ttu-id="6233d-106">La interfaz **ID3DXMatrixStack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6233d-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6233d-107">**ID3DXMatrixStack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6233d-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="6233d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6233d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6233d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6233d-109">Methods</span></span>

<span data-ttu-id="6233d-110">La interfaz **ID3DXMatrixStack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6233d-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="6233d-111">Método</span><span class="sxs-lookup"><span data-stu-id="6233d-111">Method</span></span>                                                                      | <span data-ttu-id="6233d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6233d-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6233d-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="6233d-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="6233d-114">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="6233d-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="6233d-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="6233d-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="6233d-116">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="6233d-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="6233d-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="6233d-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="6233d-118">Carga la matriz especificada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="6233d-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="6233d-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="6233d-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="6233d-120">Determina el producto de la matriz actual y la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="6233d-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="6233d-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="6233d-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="6233d-122">Determina el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="6233d-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="6233d-123">**Emergente**</span><span class="sxs-lookup"><span data-stu-id="6233d-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="6233d-124">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="6233d-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="6233d-125">**Inserción**</span><span class="sxs-lookup"><span data-stu-id="6233d-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="6233d-126">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="6233d-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="6233d-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="6233d-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="6233d-128">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="6233d-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="6233d-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="6233d-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="6233d-130">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="6233d-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="6233d-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="6233d-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="6233d-132">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="6233d-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="6233d-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="6233d-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="6233d-134">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="6233d-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="6233d-135">**Escala**</span><span class="sxs-lookup"><span data-stu-id="6233d-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="6233d-136">Escalar la matriz actual sobre el origen de la coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="6233d-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="6233d-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="6233d-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="6233d-138">Escala la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="6233d-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="6233d-139">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="6233d-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="6233d-140">Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="6233d-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="6233d-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="6233d-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="6233d-142">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="6233d-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6233d-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6233d-143">Remarks</span></span>

<span data-ttu-id="6233d-144">La interfaz ID3DX10MATRIXStack se obtiene mediante una llamada a la función [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="6233d-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="6233d-145">El tipo LPD3DX10MATRIXSTACK se define como un puntero a la interfaz **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="6233d-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="6233d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6233d-146">Requirements</span></span>



| <span data-ttu-id="6233d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="6233d-147">Requirement</span></span> | <span data-ttu-id="6233d-148">Value</span><span class="sxs-lookup"><span data-stu-id="6233d-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6233d-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6233d-149">Header</span></span><br/>  | <dl> <span data-ttu-id="6233d-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6233d-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6233d-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6233d-151">Library</span></span><br/> | <dl> <span data-ttu-id="6233d-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6233d-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6233d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="6233d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6233d-154">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6233d-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
