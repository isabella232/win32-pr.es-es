---
description: Estructura D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Estructura D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717703"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="f8b14-103">Estructura D3DXSHPRTSPLITMESHCLUSTERDATA</span><span class="sxs-lookup"><span data-stu-id="f8b14-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b14-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8b14-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="f8b14-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8b14-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8b14-106">**uVertStart**</span><span class="sxs-lookup"><span data-stu-id="f8b14-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-107">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-108">Vértice inicial en matriz de vértices reasignado.</span><span class="sxs-lookup"><span data-stu-id="f8b14-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="f8b14-109">**uVertLength**</span><span class="sxs-lookup"><span data-stu-id="f8b14-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-111">Número de vértices de este superclúster.</span><span class="sxs-lookup"><span data-stu-id="f8b14-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="f8b14-112">**uFaceStart**</span><span class="sxs-lookup"><span data-stu-id="f8b14-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-114">Índice inicial en la matriz de caras.</span><span class="sxs-lookup"><span data-stu-id="f8b14-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="f8b14-115">**uFaceLength**</span><span class="sxs-lookup"><span data-stu-id="f8b14-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-117">Número de caras de este superclúster.</span><span class="sxs-lookup"><span data-stu-id="f8b14-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="f8b14-118">**uClusterStart**</span><span class="sxs-lookup"><span data-stu-id="f8b14-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-120">Índice inicial en la matriz de clústeres.</span><span class="sxs-lookup"><span data-stu-id="f8b14-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="f8b14-121">**uClusterLength**</span><span class="sxs-lookup"><span data-stu-id="f8b14-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="f8b14-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b14-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b14-123">Número de clústeres en esta matriz supercluster.</span><span class="sxs-lookup"><span data-stu-id="f8b14-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8b14-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8b14-124">Requirements</span></span>



| <span data-ttu-id="f8b14-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b14-125">Requirement</span></span> | <span data-ttu-id="f8b14-126">Value</span><span class="sxs-lookup"><span data-stu-id="f8b14-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b14-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8b14-127">Header</span></span><br/> | <dl> <span data-ttu-id="f8b14-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b14-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b14-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8b14-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b14-130">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="f8b14-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f8b14-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="f8b14-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
