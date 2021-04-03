---
description: Crea un objeto de malla de máscara vacía mediante un declarador.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Función D3DXCreateSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914729"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="ba24e-103">D3DXCreateSkinInfo función)</span><span class="sxs-lookup"><span data-stu-id="ba24e-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="ba24e-104">Crea un objeto de malla de máscara vacía mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="ba24e-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba24e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba24e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ba24e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba24e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba24e-107">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba24e-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba24e-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba24e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba24e-109">Número de vértices para la malla de la máscara.</span><span class="sxs-lookup"><span data-stu-id="ba24e-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ba24e-110">*pDeclaration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba24e-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba24e-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba24e-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="ba24e-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="ba24e-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ba24e-113">*NumBones* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba24e-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba24e-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba24e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba24e-115">Número de huesos para la malla de la máscara.</span><span class="sxs-lookup"><span data-stu-id="ba24e-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ba24e-116">*ppSkinInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ba24e-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba24e-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba24e-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="ba24e-118">Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="ba24e-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba24e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba24e-119">Return value</span></span>

<span data-ttu-id="ba24e-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba24e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba24e-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba24e-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba24e-122">Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ba24e-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba24e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba24e-123">Remarks</span></span>

<span data-ttu-id="ba24e-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) para rellenar el objeto de malla de máscara vacía devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="ba24e-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba24e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba24e-125">Requirements</span></span>



| <span data-ttu-id="ba24e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba24e-126">Requirement</span></span> | <span data-ttu-id="ba24e-127">Value</span><span class="sxs-lookup"><span data-stu-id="ba24e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba24e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba24e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ba24e-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba24e-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ba24e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba24e-130">Library</span></span><br/> | <dl> <span data-ttu-id="ba24e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba24e-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba24e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba24e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba24e-133">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="ba24e-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ba24e-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="ba24e-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
