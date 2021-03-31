---
description: Estructura D3DXSHPRTSPLITMESHVERTDATA
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: Estructura D3DXSHPRTSPLITMESHVERTDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821055"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a><span data-ttu-id="7bb85-103">Estructura D3DXSHPRTSPLITMESHVERTDATA</span><span class="sxs-lookup"><span data-stu-id="7bb85-103">D3DXSHPRTSPLITMESHVERTDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb85-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bb85-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a><span data-ttu-id="7bb85-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bb85-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bb85-106">**uVertRemap**</span><span class="sxs-lookup"><span data-stu-id="7bb85-106">**uVertRemap**</span></span>
</dt> <dd>

<span data-ttu-id="7bb85-107">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7bb85-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7bb85-108">Vértice de la malla original. este corresponde a.</span><span class="sxs-lookup"><span data-stu-id="7bb85-108">Vertex in original mesh this corresponds to.</span></span>

</dd> <dt>

<span data-ttu-id="7bb85-109">**uSubCluster**</span><span class="sxs-lookup"><span data-stu-id="7bb85-109">**uSubCluster**</span></span>
</dt> <dd>

<span data-ttu-id="7bb85-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7bb85-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7bb85-111">Índice del clúster, en relación con el superclúster.</span><span class="sxs-lookup"><span data-stu-id="7bb85-111">Cluster index, relative to the supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="7bb85-112">**ucVertStatus**</span><span class="sxs-lookup"><span data-stu-id="7bb85-112">**ucVertStatus**</span></span>
</dt> <dd>

<span data-ttu-id="7bb85-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7bb85-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7bb85-114">1 si el vértice tiene datos válidos, 0 si es "Full".</span><span class="sxs-lookup"><span data-stu-id="7bb85-114">1 if vertex has valid data, 0 if it is "full".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bb85-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bb85-115">Remarks</span></span>

<span data-ttu-id="7bb85-116">Asignado en [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span><span class="sxs-lookup"><span data-stu-id="7bb85-116">Allocated in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb85-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bb85-117">Requirements</span></span>



| <span data-ttu-id="7bb85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb85-118">Requirement</span></span> | <span data-ttu-id="7bb85-119">Value</span><span class="sxs-lookup"><span data-stu-id="7bb85-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb85-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bb85-120">Header</span></span><br/> | <dl> <span data-ttu-id="7bb85-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bb85-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb85-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bb85-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb85-123">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="7bb85-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
