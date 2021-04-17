---
description: Concatena un grupo de mallas en una malla común. Este método puede aplicar opcionalmente una transformación de matriz a cada malla de entrada y sus coordenadas de textura.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Función D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698305"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="4ef9b-104">D3DXConcatenateMeshes función)</span><span class="sxs-lookup"><span data-stu-id="4ef9b-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="4ef9b-105">Concatena un grupo de mallas en una malla común.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="4ef9b-106">Este método puede aplicar opcionalmente una transformación de matriz a cada malla de entrada y sus coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef9b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ef9b-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="4ef9b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ef9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ef9b-109">*ppMeshes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ef9b-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="4ef9b-111">Matriz de punteros de malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="4ef9b-112">El número de elementos de la matriz es NumMeshes.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-113">*NumMeshes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ef9b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ef9b-115">Número de mallas de entrada que se van a concatenar.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-116">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ef9b-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ef9b-118">Opciones de creación de mallas; se trata de una combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="4ef9b-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="4ef9b-119">Las opciones de creación de malla son equivalentes al parámetro Options que requiere [**D3DXCreateMesh**](d3dxcreatemesh.md).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-120">*pGeomXForms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-121">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ef9b-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4ef9b-122">Matriz opcional de transformaciones de geometría.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="4ef9b-123">El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación (vea [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="4ef9b-124">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-125">*pTextureXForms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ef9b-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4ef9b-127">Matriz opcional de transformaciones de textura.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-127">Optional array of texture transforms.</span></span> <span data-ttu-id="4ef9b-128">El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación (vea [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="4ef9b-129">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-130">*pDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-131">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ef9b-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4ef9b-132">Puntero opcional a una declaración de vértice (vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="4ef9b-133">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-134">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-135">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4ef9b-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4ef9b-136">Puntero a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la nueva malla.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4ef9b-137">*ppMeshOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ef9b-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef9b-138">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ef9b-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="4ef9b-139">Dirección de un puntero a la malla creada (vea [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ef9b-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ef9b-140">Return value</span></span>

<span data-ttu-id="4ef9b-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ef9b-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ef9b-142">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4ef9b-143">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef9b-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ef9b-144">Remarks</span></span>

<span data-ttu-id="4ef9b-145">Si no se proporciona ninguna [declaración de vértice](vertex-declaration.md) como parte del parámetro de creación de malla Options, el método generará una Unión de todas las declaraciones de vértices de las submallas, promoviendo canales y tipos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="4ef9b-146">El método creará una tabla de atributos a partir de las tablas de atributos de las mallas de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ef9b-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="4ef9b-147">Para garantizar la creación de una tabla de atributos, llame a [**Optimize**](id3dxmesh--optimize.md) with Flags establecido en D3DXMESHOPT \_ Compact y D3DXMESHOPT \_ ATTRSORT (consulte [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="4ef9b-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef9b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ef9b-148">Requirements</span></span>



| <span data-ttu-id="4ef9b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ef9b-149">Requirement</span></span> | <span data-ttu-id="4ef9b-150">Value</span><span class="sxs-lookup"><span data-stu-id="4ef9b-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef9b-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ef9b-151">Header</span></span><br/>  | <dl> <span data-ttu-id="4ef9b-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ef9b-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4ef9b-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ef9b-153">Library</span></span><br/> | <dl> <span data-ttu-id="4ef9b-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ef9b-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ef9b-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ef9b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef9b-156">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="4ef9b-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
