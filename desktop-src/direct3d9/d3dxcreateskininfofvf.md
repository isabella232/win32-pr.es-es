---
description: Crea un objeto de malla de máscara vacía con un código de formato de vértice flexible (FVF).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Función D3DXCreateSkinInfoFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718216"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="2dec5-103">D3DXCreateSkinInfoFVF función)</span><span class="sxs-lookup"><span data-stu-id="2dec5-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="2dec5-104">Crea un objeto de malla de máscara vacía con un código de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="2dec5-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dec5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dec5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2dec5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dec5-107">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2dec5-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dec5-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dec5-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2dec5-109">Número de vértices para la malla de la máscara.</span><span class="sxs-lookup"><span data-stu-id="2dec5-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2dec5-110">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2dec5-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dec5-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dec5-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2dec5-112">Combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértice de la malla de máscara devuelta.</span><span class="sxs-lookup"><span data-stu-id="2dec5-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2dec5-113">*NumBones* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2dec5-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dec5-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dec5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2dec5-115">Número de huesos para la malla de la máscara.</span><span class="sxs-lookup"><span data-stu-id="2dec5-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2dec5-116">*ppSkinInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2dec5-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dec5-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="2dec5-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="2dec5-118">Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) que representa el objeto de información de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="2dec5-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dec5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dec5-119">Return value</span></span>

<span data-ttu-id="2dec5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2dec5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2dec5-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2dec5-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2dec5-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2dec5-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dec5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dec5-123">Remarks</span></span>

<span data-ttu-id="2dec5-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) para rellenar el objeto de malla de máscara vacía devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="2dec5-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dec5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dec5-125">Requirements</span></span>



| <span data-ttu-id="2dec5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dec5-126">Requirement</span></span> | <span data-ttu-id="2dec5-127">Value</span><span class="sxs-lookup"><span data-stu-id="2dec5-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dec5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dec5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2dec5-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dec5-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2dec5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2dec5-130">Library</span></span><br/> | <dl> <span data-ttu-id="2dec5-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dec5-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2dec5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dec5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dec5-133">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="2dec5-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="2dec5-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="2dec5-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
