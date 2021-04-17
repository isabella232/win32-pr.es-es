---
description: Convierte el subconjunto de malla especificado en una franja de triángulo única.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Función D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670219"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="106e9-103">D3DXConvertMeshSubsetToSingleStrip función)</span><span class="sxs-lookup"><span data-stu-id="106e9-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="106e9-104">Convierte el subconjunto de malla especificado en una franja de triángulo única.</span><span class="sxs-lookup"><span data-stu-id="106e9-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="106e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="106e9-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="106e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="106e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="106e9-107">*Malla* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="106e9-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="106e9-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="106e9-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="106e9-109">Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a convertir en una franja.</span><span class="sxs-lookup"><span data-stu-id="106e9-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="106e9-110">*AttribId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="106e9-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="106e9-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="106e9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="106e9-112">IDENTIFICADOR de atributo del subconjunto de la malla que se va a convertir en franjas.</span><span class="sxs-lookup"><span data-stu-id="106e9-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="106e9-113">*IBOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="106e9-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="106e9-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="106e9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="106e9-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones para crear el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="106e9-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="106e9-116">No se puede D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="106e9-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="106e9-117">El búfer de índice se creará con índices de 32 bits o de 16 bits, en función del formato del búfer de índice de la malla especificada por el parámetro *meshen* .</span><span class="sxs-lookup"><span data-stu-id="106e9-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="106e9-118">*ppIndexBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="106e9-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="106e9-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="106e9-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="106e9-120">Puntero a una interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) que representa el búfer de índice que contiene la franja.</span><span class="sxs-lookup"><span data-stu-id="106e9-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="106e9-121">*pNumIndices* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="106e9-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="106e9-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="106e9-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="106e9-123">Número de índices en el búfer devuelto en el parámetro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="106e9-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="106e9-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="106e9-124">Return value</span></span>

<span data-ttu-id="106e9-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="106e9-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="106e9-126">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="106e9-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="106e9-127">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="106e9-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="106e9-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="106e9-128">Remarks</span></span>

<span data-ttu-id="106e9-129">Antes de ejecutar esta función, llame a [**Optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con el \_ indicador D3DXMESHOPT ATTRSORT establecido.</span><span class="sxs-lookup"><span data-stu-id="106e9-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="106e9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="106e9-130">Requirements</span></span>



| <span data-ttu-id="106e9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="106e9-131">Requirement</span></span> | <span data-ttu-id="106e9-132">Value</span><span class="sxs-lookup"><span data-stu-id="106e9-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="106e9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="106e9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="106e9-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="106e9-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="106e9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="106e9-135">Library</span></span><br/> | <dl> <span data-ttu-id="106e9-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="106e9-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="106e9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="106e9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106e9-138">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="106e9-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
