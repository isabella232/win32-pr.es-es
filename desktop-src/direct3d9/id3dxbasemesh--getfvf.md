---
description: 'Método ID3DXBaseMesh::GetFVF: obtiene el valor fijo del vértice de la función.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: Método ID3DXBaseMesh::GetFVF (D3DX9Mesh.h)
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
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115443"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="b7474-103">Método ID3DXBaseMesh::GetFVF</span><span class="sxs-lookup"><span data-stu-id="b7474-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="b7474-104">Obtiene el valor fijo del vértice de la función.</span><span class="sxs-lookup"><span data-stu-id="b7474-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7474-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7474-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="b7474-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7474-106">Parameters</span></span>

<span data-ttu-id="b7474-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b7474-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7474-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7474-108">Return value</span></span>

<span data-ttu-id="b7474-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7474-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7474-110">Devuelve los códigos de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="b7474-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7474-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7474-111">Remarks</span></span>

<span data-ttu-id="b7474-112">Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF.</span><span class="sxs-lookup"><span data-stu-id="b7474-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="b7474-113">Esto ocurrirá para una malla creada a partir de una declaración de vértice que no tenga el mismo orden y elementos admitidos por los códigos FVF.</span><span class="sxs-lookup"><span data-stu-id="b7474-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7474-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7474-114">Requirements</span></span>



| <span data-ttu-id="b7474-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7474-115">Requirement</span></span> | <span data-ttu-id="b7474-116">Value</span><span class="sxs-lookup"><span data-stu-id="b7474-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7474-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7474-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b7474-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7474-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b7474-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7474-119">Library</span></span><br/> | <dl> <span data-ttu-id="b7474-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7474-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7474-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7474-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7474-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b7474-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
