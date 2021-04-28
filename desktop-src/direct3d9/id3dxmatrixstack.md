---
description: 'Interfaz ID3DXMATRIXStack: las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.'
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interfaz ID3DXMATRIXStack (D3dx9math.h)
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
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093323"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="e714c-103">Interfaz ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e714c-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="e714c-104">Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.</span><span class="sxs-lookup"><span data-stu-id="e714c-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="e714c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e714c-105">Members</span></span>

<span data-ttu-id="e714c-106">La **interfaz ID3DXMATRIXStack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="e714c-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e714c-107">**ID3DXMATRIXStack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e714c-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="e714c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e714c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e714c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e714c-109">Methods</span></span>

<span data-ttu-id="e714c-110">La **interfaz ID3DXMATRIXStack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e714c-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="e714c-111">Método</span><span class="sxs-lookup"><span data-stu-id="e714c-111">Method</span></span>                                                                       | <span data-ttu-id="e714c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e714c-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e714c-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="e714c-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="e714c-114">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="e714c-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="e714c-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e714c-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="e714c-116">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e714c-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e714c-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="e714c-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="e714c-118">Carga la matriz dada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e714c-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="e714c-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e714c-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="e714c-120">Determina el producto de la matriz actual y la matriz dada.</span><span class="sxs-lookup"><span data-stu-id="e714c-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="e714c-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="e714c-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="e714c-122">Determina el producto de la matriz dada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e714c-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="e714c-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="e714c-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="e714c-124">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="e714c-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="e714c-125">**Insertar**</span><span class="sxs-lookup"><span data-stu-id="e714c-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="e714c-126">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="e714c-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="e714c-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="e714c-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="e714c-128">Gira (en relación con el espacio de coordenadas del mundo) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e714c-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="e714c-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="e714c-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="e714c-130">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e714c-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="e714c-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e714c-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="e714c-132">Gira (en relación con el espacio de coordenadas del mundo) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e714c-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="e714c-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="e714c-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="e714c-134">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e714c-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="e714c-135">**Escala**</span><span class="sxs-lookup"><span data-stu-id="e714c-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="e714c-136">Escale la matriz actual sobre el origen de coordenadas del mundo.</span><span class="sxs-lookup"><span data-stu-id="e714c-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="e714c-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="e714c-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="e714c-138">Escale la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="e714c-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="e714c-139">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="e714c-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="e714c-140">Determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="e714c-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="e714c-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="e714c-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="e714c-142">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e714c-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e714c-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e714c-143">Remarks</span></span>

<span data-ttu-id="e714c-144">La **interfaz ID3DXMATRIXStack** se obtiene llamando a la función [**D3DXCreateMatrixStack.**](d3dxcreatematrixstack.md)</span><span class="sxs-lookup"><span data-stu-id="e714c-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="e714c-145">El tipo LPD3DXMATRIXSTACK se define como un puntero a la **interfaz ID3DXMATRIXStack.**</span><span class="sxs-lookup"><span data-stu-id="e714c-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="e714c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e714c-146">Requirements</span></span>



| <span data-ttu-id="e714c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e714c-147">Requirement</span></span> | <span data-ttu-id="e714c-148">Value</span><span class="sxs-lookup"><span data-stu-id="e714c-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e714c-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e714c-149">Header</span></span><br/>  | <dl> <span data-ttu-id="e714c-150"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e714c-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e714c-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e714c-151">Library</span></span><br/> | <dl> <span data-ttu-id="e714c-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e714c-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e714c-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e714c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e714c-154">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="e714c-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
