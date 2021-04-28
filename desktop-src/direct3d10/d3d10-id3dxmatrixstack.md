---
description: 'Interfaz ID3DXMatrixStack: las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.'
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interfaz ID3DXMatrixStack (D3DX10.h)
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
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094413"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="784a3-103">Interfaz ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="784a3-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="784a3-104">Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.</span><span class="sxs-lookup"><span data-stu-id="784a3-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="784a3-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="784a3-105">Members</span></span>

<span data-ttu-id="784a3-106">La **interfaz ID3DXMatrixStack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="784a3-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="784a3-107">**ID3DXMatrixStack también** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="784a3-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="784a3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="784a3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="784a3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="784a3-109">Methods</span></span>

<span data-ttu-id="784a3-110">La **interfaz ID3DXMatrixStack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="784a3-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="784a3-111">Método</span><span class="sxs-lookup"><span data-stu-id="784a3-111">Method</span></span>                                                                      | <span data-ttu-id="784a3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="784a3-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="784a3-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="784a3-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="784a3-114">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="784a3-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="784a3-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="784a3-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="784a3-116">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="784a3-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="784a3-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="784a3-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="784a3-118">Carga la matriz dada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="784a3-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="784a3-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="784a3-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="784a3-120">Determina el producto de la matriz actual y la matriz dada.</span><span class="sxs-lookup"><span data-stu-id="784a3-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="784a3-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="784a3-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="784a3-122">Determina el producto de la matriz dada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="784a3-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="784a3-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="784a3-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="784a3-124">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="784a3-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="784a3-125">**Insertar**</span><span class="sxs-lookup"><span data-stu-id="784a3-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="784a3-126">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="784a3-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="784a3-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="784a3-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="784a3-128">Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="784a3-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="784a3-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="784a3-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="784a3-130">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="784a3-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="784a3-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="784a3-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="784a3-132">Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="784a3-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="784a3-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="784a3-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="784a3-134">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="784a3-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="784a3-135">**Escala**</span><span class="sxs-lookup"><span data-stu-id="784a3-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="784a3-136">Escale la matriz actual sobre el origen de la coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="784a3-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="784a3-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="784a3-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="784a3-138">Escale la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="784a3-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="784a3-139">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="784a3-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="784a3-140">Determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="784a3-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="784a3-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="784a3-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="784a3-142">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="784a3-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="784a3-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="784a3-143">Remarks</span></span>

<span data-ttu-id="784a3-144">La interfaz ID3DX10MATRIXStack se obtiene mediante una llamada a la función [**D3DXCreateMatrixStack.**](d3d10-d3dxcreatematrixstack.md)</span><span class="sxs-lookup"><span data-stu-id="784a3-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="784a3-145">El tipo LPD3DX10MATRIXSTACK se define como un puntero a la **interfaz ID3DXMatrixStack.**</span><span class="sxs-lookup"><span data-stu-id="784a3-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="784a3-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="784a3-146">Requirements</span></span>



| <span data-ttu-id="784a3-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="784a3-147">Requirement</span></span> | <span data-ttu-id="784a3-148">Value</span><span class="sxs-lookup"><span data-stu-id="784a3-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="784a3-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="784a3-149">Header</span></span><br/>  | <dl> <span data-ttu-id="784a3-150"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="784a3-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="784a3-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="784a3-151">Library</span></span><br/> | <dl> <span data-ttu-id="784a3-152"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="784a3-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="784a3-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="784a3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784a3-154">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="784a3-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
