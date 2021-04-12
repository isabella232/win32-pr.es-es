---
description: Encapsula un marco de transformación en una jerarquía de fotogramas de transformación.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Estructura D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280320"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="287b8-103">Estructura D3DXFRAME</span><span class="sxs-lookup"><span data-stu-id="287b8-103">D3DXFRAME structure</span></span>

<span data-ttu-id="287b8-104">Encapsula un marco de transformación en una jerarquía de fotogramas de transformación.</span><span class="sxs-lookup"><span data-stu-id="287b8-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="287b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="287b8-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="287b8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="287b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="287b8-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="287b8-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="287b8-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="287b8-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="287b8-109">Nombre del marco.</span><span class="sxs-lookup"><span data-stu-id="287b8-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="287b8-110">**TransformationMatrix**</span><span class="sxs-lookup"><span data-stu-id="287b8-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="287b8-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="287b8-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="287b8-112">Matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="287b8-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="287b8-113">**pMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="287b8-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="287b8-114">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="287b8-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="287b8-115">Puntero al contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="287b8-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="287b8-116">**pFrameSibling**</span><span class="sxs-lookup"><span data-stu-id="287b8-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="287b8-117">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="287b8-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="287b8-118">Puntero a un marco relacionado.</span><span class="sxs-lookup"><span data-stu-id="287b8-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="287b8-119">**pFrameFirstChild**</span><span class="sxs-lookup"><span data-stu-id="287b8-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="287b8-120">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="287b8-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="287b8-121">Puntero a un marco secundario.</span><span class="sxs-lookup"><span data-stu-id="287b8-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="287b8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="287b8-122">Remarks</span></span>

<span data-ttu-id="287b8-123">Una aplicación puede derivar de esta estructura para agregar otros datos.</span><span class="sxs-lookup"><span data-stu-id="287b8-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="287b8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="287b8-124">Requirements</span></span>



| <span data-ttu-id="287b8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="287b8-125">Requirement</span></span> | <span data-ttu-id="287b8-126">Value</span><span class="sxs-lookup"><span data-stu-id="287b8-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="287b8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="287b8-127">Header</span></span><br/> | <dl> <span data-ttu-id="287b8-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="287b8-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="287b8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="287b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="287b8-130">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="287b8-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




