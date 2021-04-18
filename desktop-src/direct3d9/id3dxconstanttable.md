---
description: La interfaz ID3DXConstantTable se usa para tener acceso a la tabla de constantes. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaz ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718245"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="4f986-104">Interfaz ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="4f986-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="4f986-105">La interfaz ID3DXConstantTable se usa para tener acceso a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="4f986-106">Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="4f986-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="4f986-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f986-107">Members</span></span>

<span data-ttu-id="4f986-108">La interfaz **ID3DXConstantTable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4f986-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f986-109">**ID3DXConstantTable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f986-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="4f986-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f986-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f986-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f986-111">Methods</span></span>

<span data-ttu-id="4f986-112">La interfaz **ID3DXConstantTable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4f986-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="4f986-113">Método</span><span class="sxs-lookup"><span data-stu-id="4f986-113">Method</span></span>                                                                                       | <span data-ttu-id="4f986-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f986-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f986-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="4f986-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="4f986-116">Obtiene un puntero al búfer que contiene la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="4f986-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="4f986-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="4f986-118">Obtiene el tamaño de búfer de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="4f986-119">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="4f986-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="4f986-120">Obtiene una constante mediante la búsqueda de su índice.</span><span class="sxs-lookup"><span data-stu-id="4f986-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="4f986-121">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="4f986-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="4f986-122">Obtiene una constante buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="4f986-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="4f986-123">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="4f986-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="4f986-124">Obtiene un puntero a una matriz de descripciones constantes en la tabla Constant.</span><span class="sxs-lookup"><span data-stu-id="4f986-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="4f986-125">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="4f986-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="4f986-126">Obtiene una constante de una matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="4f986-127">Una matriz se compone de elementos.</span><span class="sxs-lookup"><span data-stu-id="4f986-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="4f986-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4f986-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="4f986-129">Obtiene una descripción de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="4f986-130">**GetSamplerIndex**</span><span class="sxs-lookup"><span data-stu-id="4f986-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="4f986-131">Devuelve el índice de muestra.</span><span class="sxs-lookup"><span data-stu-id="4f986-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4f986-132">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="4f986-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="4f986-133">Establece un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="4f986-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="4f986-134">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="4f986-135">Establece una matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="4f986-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="4f986-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="4f986-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="4f986-137">Establece las constantes en sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4f986-137">Sets the constants to their default values.</span></span> <span data-ttu-id="4f986-138">Los valores predeterminados se declaran en las declaraciones de variable en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f986-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="4f986-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="4f986-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="4f986-140">Establece un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="4f986-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4f986-141">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="4f986-142">Establece una matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="4f986-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="4f986-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="4f986-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="4f986-144">Establece un valor entero.</span><span class="sxs-lookup"><span data-stu-id="4f986-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="4f986-145">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="4f986-146">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="4f986-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4f986-147">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="4f986-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="4f986-148">Establece una matriz de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="4f986-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="4f986-149">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="4f986-150">Establece una matriz de matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="4f986-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="4f986-151">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="4f986-152">Establece una matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="4f986-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="4f986-153">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="4f986-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="4f986-154">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="4f986-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4f986-155">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="4f986-156">Establece una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="4f986-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="4f986-157">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="4f986-158">Establece una matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="4f986-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="4f986-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="4f986-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="4f986-160">Establece el contenido del búfer en la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f986-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="4f986-161">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="4f986-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="4f986-162">Establece un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="4f986-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4f986-163">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="4f986-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="4f986-164">Establece una matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="4f986-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4f986-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f986-165">Remarks</span></span>

<span data-ttu-id="4f986-166">El tipo LPD3DXCONSTANTTABLE se define como un puntero a la interfaz **ID3DXConstantTable** .</span><span class="sxs-lookup"><span data-stu-id="4f986-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="4f986-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f986-167">Requirements</span></span>



| <span data-ttu-id="4f986-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f986-168">Requirement</span></span> | <span data-ttu-id="4f986-169">Value</span><span class="sxs-lookup"><span data-stu-id="4f986-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f986-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f986-170">Header</span></span><br/>  | <dl> <span data-ttu-id="4f986-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f986-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4f986-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f986-172">Library</span></span><br/> | <dl> <span data-ttu-id="4f986-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f986-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4f986-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f986-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f986-175">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="4f986-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
