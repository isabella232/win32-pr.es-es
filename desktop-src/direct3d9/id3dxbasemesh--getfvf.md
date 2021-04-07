---
description: Obtiene el valor de vértice de función fijo.
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'ID3DXBaseMesh:: GetFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003856"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="188b3-103">ID3DXBaseMesh:: GetFVF (método)</span><span class="sxs-lookup"><span data-stu-id="188b3-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="188b3-104">Obtiene el valor de vértice de función fijo.</span><span class="sxs-lookup"><span data-stu-id="188b3-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="188b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="188b3-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="188b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="188b3-106">Parameters</span></span>

<span data-ttu-id="188b3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="188b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="188b3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="188b3-108">Return value</span></span>

<span data-ttu-id="188b3-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="188b3-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="188b3-110">Devuelve los códigos de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="188b3-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="188b3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="188b3-111">Remarks</span></span>

<span data-ttu-id="188b3-112">Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF.</span><span class="sxs-lookup"><span data-stu-id="188b3-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="188b3-113">Esto ocurrirá en una malla creada a partir de una declaración de vértices que no tiene el mismo orden y los mismos elementos que los códigos de FVF.</span><span class="sxs-lookup"><span data-stu-id="188b3-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="188b3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="188b3-114">Requirements</span></span>



| <span data-ttu-id="188b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="188b3-115">Requirement</span></span> | <span data-ttu-id="188b3-116">Value</span><span class="sxs-lookup"><span data-stu-id="188b3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="188b3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="188b3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="188b3-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="188b3-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="188b3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="188b3-119">Library</span></span><br/> | <dl> <span data-ttu-id="188b3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="188b3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="188b3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="188b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188b3-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="188b3-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
