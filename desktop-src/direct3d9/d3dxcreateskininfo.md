---
description: 'Función D3DXCreateSkinInfo: crea un objeto de malla de máscara vacía mediante un declarador.'
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Función D3DXCreateSkinInfo (D3DX9Mesh.h)
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
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102743"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="28201-103">Función D3DXCreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="28201-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="28201-104">Crea un objeto de malla de máscara vacía mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="28201-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="28201-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28201-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="28201-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28201-107">*NumVertices* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28201-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28201-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28201-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28201-109">Número de vértices para la malla de máscara.</span><span class="sxs-lookup"><span data-stu-id="28201-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="28201-110">*pDeclaration* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28201-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28201-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="28201-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="28201-112">Matriz de [**elementos D3DVERTEXELEMENT9,**](d3dvertexelement9.md) que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="28201-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="28201-113">*Num Num* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28201-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28201-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28201-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28201-115">Número de tejidos para la malla de máscara.</span><span class="sxs-lookup"><span data-stu-id="28201-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="28201-116">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28201-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28201-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="28201-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="28201-118">Dirección de un puntero a una [**interfaz ID3DXSkinInfo,**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="28201-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28201-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28201-119">Return value</span></span>

<span data-ttu-id="28201-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28201-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28201-121">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28201-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="28201-122">Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="28201-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="28201-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28201-123">Remarks</span></span>

<span data-ttu-id="28201-124">Use [**SetIonalInfluence para**](id3dxskininfo--setboneinfluence.md) rellenar el objeto de malla de máscara vacío devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="28201-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="28201-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28201-125">Requirements</span></span>



| <span data-ttu-id="28201-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="28201-126">Requirement</span></span> | <span data-ttu-id="28201-127">Value</span><span class="sxs-lookup"><span data-stu-id="28201-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28201-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28201-128">Header</span></span><br/>  | <dl> <span data-ttu-id="28201-129"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="28201-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="28201-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28201-130">Library</span></span><br/> | <dl> <span data-ttu-id="28201-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="28201-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28201-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28201-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28201-133">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="28201-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="28201-134">**SetIonalInfluence**</span><span class="sxs-lookup"><span data-stu-id="28201-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
