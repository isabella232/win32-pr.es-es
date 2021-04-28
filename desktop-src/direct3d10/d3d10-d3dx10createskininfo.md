---
description: 'Función D3DX10CreateSkinInfo: crea un objeto de malla de máscara vacía mediante un declarador.'
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Función D3DX10CreateSkinInfo (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103603"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="cc2d4-103">Función D3DX10CreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="cc2d4-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="cc2d4-104">Crea un objeto de malla de máscara vacía mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="cc2d4-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc2d4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cc2d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc2d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc2d4-107">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc2d4-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2d4-108">Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc2d4-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="cc2d4-109">Dirección de un puntero a una [**interfaz ID3DX10SkinInfo**](id3dx10skininfo.md), que representa el objeto de malla de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="cc2d4-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc2d4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc2d4-110">Return value</span></span>

<span data-ttu-id="cc2d4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc2d4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc2d4-112">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc2d4-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc2d4-113">Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc2d4-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc2d4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc2d4-114">Remarks</span></span>

<span data-ttu-id="cc2d4-115">Use [**id3DX10SkinInfo::SetIonalInfluence para**](id3dx10skininfo-setboneinfluence.md) rellenar el objeto de malla de máscara vacío devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="cc2d4-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2d4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2d4-116">Requirements</span></span>



| <span data-ttu-id="cc2d4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2d4-117">Requirement</span></span> | <span data-ttu-id="cc2d4-118">Value</span><span class="sxs-lookup"><span data-stu-id="cc2d4-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2d4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc2d4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc2d4-120"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="cc2d4-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cc2d4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc2d4-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc2d4-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc2d4-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc2d4-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc2d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2d4-124">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="cc2d4-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="cc2d4-125">Funciones D3DX</span><span class="sxs-lookup"><span data-stu-id="cc2d4-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




