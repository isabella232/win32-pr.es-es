---
description: Crea un objeto de malla de máscara vacía mediante un declarador.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Función D3DX10CreateSkinInfo (D3DX10Mesh. h)
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
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689892"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="6a221-103">D3DX10CreateSkinInfo función)</span><span class="sxs-lookup"><span data-stu-id="6a221-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="6a221-104">Crea un objeto de malla de máscara vacía mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="6a221-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a221-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a221-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6a221-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a221-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a221-107">*ppSkinInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6a221-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a221-108">Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a221-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="6a221-109">Dirección de un puntero a una [**interfaz ID3DX10SkinInfo**](id3dx10skininfo.md)que representa el objeto de malla de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="6a221-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a221-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a221-110">Return value</span></span>

<span data-ttu-id="6a221-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a221-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a221-112">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a221-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a221-113">Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6a221-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a221-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a221-114">Remarks</span></span>

<span data-ttu-id="6a221-115">Use [**ID3DX10SkinInfo:: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) para rellenar el objeto de malla de máscara vacía devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="6a221-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a221-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a221-116">Requirements</span></span>



| <span data-ttu-id="6a221-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a221-117">Requirement</span></span> | <span data-ttu-id="6a221-118">Value</span><span class="sxs-lookup"><span data-stu-id="6a221-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a221-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a221-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6a221-120"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a221-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6a221-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a221-121">Library</span></span><br/> | <dl> <span data-ttu-id="6a221-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a221-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a221-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a221-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a221-124">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="6a221-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6a221-125">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="6a221-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




