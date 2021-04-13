---
description: Describe un volumen.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: D3DVOLUME_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362637"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="94976-103">D3DVOLUME \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="94976-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="94976-104">Describe un volumen.</span><span class="sxs-lookup"><span data-stu-id="94976-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="94976-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94976-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="94976-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="94976-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="94976-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="94976-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="94976-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-109">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie del volumen.</span><span class="sxs-lookup"><span data-stu-id="94976-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="94976-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="94976-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="94976-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-112">Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como un volumen.</span><span class="sxs-lookup"><span data-stu-id="94976-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="94976-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="94976-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="94976-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-115">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="94976-115">Currently not used.</span></span> <span data-ttu-id="94976-116">Siempre se devuelve como 0.</span><span class="sxs-lookup"><span data-stu-id="94976-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="94976-117">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="94976-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="94976-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-119">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para este volumen.</span><span class="sxs-lookup"><span data-stu-id="94976-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="94976-120">**Width**</span><span class="sxs-lookup"><span data-stu-id="94976-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="94976-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-122">Ancho del volumen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94976-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="94976-123">**Height**</span><span class="sxs-lookup"><span data-stu-id="94976-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="94976-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-125">Alto del volumen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94976-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="94976-126">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="94976-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="94976-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94976-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94976-128">Profundidad del volumen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94976-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94976-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94976-129">Requirements</span></span>



| <span data-ttu-id="94976-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="94976-130">Requirement</span></span> | <span data-ttu-id="94976-131">Value</span><span class="sxs-lookup"><span data-stu-id="94976-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94976-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94976-132">Header</span></span><br/> | <dl> <span data-ttu-id="94976-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="94976-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94976-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="94976-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94976-135">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="94976-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="94976-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="94976-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="94976-137">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="94976-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
