---
description: La interfaz ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interfaz ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670226"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="6a466-103">Interfaz ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="6a466-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="6a466-104">La interfaz ID3DXTextureShader.</span><span class="sxs-lookup"><span data-stu-id="6a466-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="6a466-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a466-105">Members</span></span>

<span data-ttu-id="6a466-106">La interfaz **ID3DXTextureShader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6a466-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a466-107">**ID3DXTextureShader** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a466-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="6a466-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a466-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a466-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a466-109">Methods</span></span>

<span data-ttu-id="6a466-110">La interfaz **ID3DXTextureShader** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6a466-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="6a466-111">Método</span><span class="sxs-lookup"><span data-stu-id="6a466-111">Method</span></span>                                                                                       | <span data-ttu-id="6a466-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a466-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="6a466-113">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="6a466-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="6a466-114">Obtiene una constante mediante la búsqueda de su índice.</span><span class="sxs-lookup"><span data-stu-id="6a466-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="6a466-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="6a466-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="6a466-116">Obtiene un puntero a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a466-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="6a466-117">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="6a466-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="6a466-118">Obtiene una constante buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="6a466-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="6a466-119">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="6a466-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="6a466-120">Obtiene un puntero a la matriz de constantes de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a466-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="6a466-121">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="6a466-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="6a466-122">Obtiene una constante de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a466-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="6a466-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="6a466-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="6a466-124">Obtiene una descripción de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a466-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="6a466-125">**GetFunction (**</span><span class="sxs-lookup"><span data-stu-id="6a466-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="6a466-126">Obtiene un puntero a la secuencia DWORD de la función.</span><span class="sxs-lookup"><span data-stu-id="6a466-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="6a466-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="6a466-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="6a466-128">Establece un valor BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="6a466-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="6a466-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="6a466-130">Establece una matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="6a466-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="6a466-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="6a466-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="6a466-132">Establece las constantes en los valores predeterminados declarados en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a466-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="6a466-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="6a466-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="6a466-134">Establece un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="6a466-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="6a466-135">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="6a466-136">Establece una matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="6a466-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="6a466-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="6a466-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="6a466-138">Establece un valor entero.</span><span class="sxs-lookup"><span data-stu-id="6a466-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="6a466-139">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="6a466-140">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="6a466-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="6a466-141">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="6a466-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="6a466-142">Establece una matriz no transpuesta.</span><span class="sxs-lookup"><span data-stu-id="6a466-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="6a466-143">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="6a466-144">Establece una matriz de matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a466-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="6a466-145">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="6a466-146">Establece una matriz de punteros a matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a466-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="6a466-147">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="6a466-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="6a466-148">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="6a466-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="6a466-149">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="6a466-150">Establece una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a466-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="6a466-151">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="6a466-152">Establece una matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a466-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="6a466-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="6a466-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="6a466-154">Establece la tabla de constantes con los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="6a466-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="6a466-155">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="6a466-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="6a466-156">Establece un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="6a466-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="6a466-157">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="6a466-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="6a466-158">Establece una matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="6a466-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="6a466-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a466-159">Remarks</span></span>

<span data-ttu-id="6a466-160">La interfaz **ID3DXTextureShader** se obtiene mediante una llamada a la función [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="6a466-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="6a466-161">La interfaz **ID3DXTextureShader** , al igual que todas las interfaces com, hereda la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6a466-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="6a466-162">El tipo LPD3DXTEXTURESHADER se define como un puntero a la interfaz **ID3DXTextureShader** .</span><span class="sxs-lookup"><span data-stu-id="6a466-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="6a466-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a466-163">Requirements</span></span>



| <span data-ttu-id="6a466-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a466-164">Requirement</span></span> | <span data-ttu-id="6a466-165">Value</span><span class="sxs-lookup"><span data-stu-id="6a466-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a466-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a466-166">Header</span></span><br/>  | <dl> <span data-ttu-id="6a466-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a466-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6a466-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a466-168">Library</span></span><br/> | <dl> <span data-ttu-id="6a466-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a466-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6a466-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a466-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a466-171">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6a466-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
