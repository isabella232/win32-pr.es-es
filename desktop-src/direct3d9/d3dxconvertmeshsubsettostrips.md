---
description: Convierte el subconjunto de malla especificado en una serie de bandas.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Función D3DXConvertMeshSubsetToStrips (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708045"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="31d21-103">D3DXConvertMeshSubsetToStrips función)</span><span class="sxs-lookup"><span data-stu-id="31d21-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="31d21-104">Convierte el subconjunto de malla especificado en una serie de bandas.</span><span class="sxs-lookup"><span data-stu-id="31d21-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31d21-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="31d21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31d21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d21-107">*Malla* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31d21-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="31d21-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="31d21-109">Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a convertir en una franja.</span><span class="sxs-lookup"><span data-stu-id="31d21-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-110">*AttribId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31d21-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31d21-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31d21-112">IDENTIFICADOR de atributo del subconjunto de la malla que se va a convertir en franjas.</span><span class="sxs-lookup"><span data-stu-id="31d21-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-113">*IBOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31d21-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31d21-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31d21-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones para crear el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="31d21-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="31d21-116">No se puede D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="31d21-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="31d21-117">El búfer de índice se creará con índices de 32 bits o de 16 bits, en función del formato del búfer de índice de la malla especificada por el parámetro *meshen* .</span><span class="sxs-lookup"><span data-stu-id="31d21-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-118">*ppIndexBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31d21-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="31d21-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="31d21-120">Puntero a una interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) que representa el búfer de índice que contiene la franja.</span><span class="sxs-lookup"><span data-stu-id="31d21-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-121">*pNumIndices* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31d21-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31d21-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31d21-123">Número de índices en el búfer devuelto en el parámetro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="31d21-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-124">*ppStripLengths* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31d21-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="31d21-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="31d21-126">Búfer que contiene una matriz de un valor DWORD por franja, que especifica el número de triángulos de la franja.</span><span class="sxs-lookup"><span data-stu-id="31d21-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="31d21-127">*pNumStrips* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31d21-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d21-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31d21-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31d21-129">Número de bandas individuales en el búfer de índice y la matriz de longitud de franja correspondiente.</span><span class="sxs-lookup"><span data-stu-id="31d21-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d21-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31d21-130">Return value</span></span>

<span data-ttu-id="31d21-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31d21-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31d21-132">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31d21-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31d21-133">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="31d21-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d21-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31d21-134">Remarks</span></span>

<span data-ttu-id="31d21-135">Antes de ejecutar esta función, llame a [**Optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con el \_ indicador D3DXMESHOPT ATTRSORT establecido.</span><span class="sxs-lookup"><span data-stu-id="31d21-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d21-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31d21-136">Requirements</span></span>



| <span data-ttu-id="31d21-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d21-137">Requirement</span></span> | <span data-ttu-id="31d21-138">Value</span><span class="sxs-lookup"><span data-stu-id="31d21-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31d21-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31d21-139">Header</span></span><br/>  | <dl> <span data-ttu-id="31d21-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d21-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31d21-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31d21-141">Library</span></span><br/> | <dl> <span data-ttu-id="31d21-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31d21-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31d21-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="31d21-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d21-144">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="31d21-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
