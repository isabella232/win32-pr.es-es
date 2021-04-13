---
description: Obtiene el valor de vértice de función fijo.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo:: GetFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362413"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="5f39f-103">ID3DXSkinInfo:: GetFVF (método)</span><span class="sxs-lookup"><span data-stu-id="5f39f-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="5f39f-104">Obtiene el valor de vértice de función fijo.</span><span class="sxs-lookup"><span data-stu-id="5f39f-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f39f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f39f-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="5f39f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f39f-106">Parameters</span></span>

<span data-ttu-id="5f39f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5f39f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f39f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f39f-108">Return value</span></span>

<span data-ttu-id="5f39f-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f39f-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f39f-110">Devuelve los códigos de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="5f39f-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f39f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f39f-111">Remarks</span></span>

<span data-ttu-id="5f39f-112">Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF.</span><span class="sxs-lookup"><span data-stu-id="5f39f-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="5f39f-113">Esto ocurrirá en una malla creada a partir de una declaración de vértices que no tiene el mismo orden y los mismos elementos que los códigos de FVF.</span><span class="sxs-lookup"><span data-stu-id="5f39f-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f39f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f39f-114">Requirements</span></span>



| <span data-ttu-id="5f39f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f39f-115">Requirement</span></span> | <span data-ttu-id="5f39f-116">Value</span><span class="sxs-lookup"><span data-stu-id="5f39f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f39f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f39f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5f39f-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f39f-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f39f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f39f-119">Library</span></span><br/> | <dl> <span data-ttu-id="5f39f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f39f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f39f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f39f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f39f-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5f39f-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="5f39f-123">**ID3DXSkinInfo::SetFVF**</span><span class="sxs-lookup"><span data-stu-id="5f39f-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
