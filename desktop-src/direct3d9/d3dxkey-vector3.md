---
description: Describe una clave vectorial para su uso en la animación de fotogramas clave. Especifica un vector en un momento dado. Se usa para las claves de escala y traducción.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3 estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721455"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="fef16-105">D3DXKEY \_ VECTOR3 (estructura)</span><span class="sxs-lookup"><span data-stu-id="fef16-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="fef16-106">Describe una clave vectorial para su uso en la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="fef16-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="fef16-107">Especifica un vector en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="fef16-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="fef16-108">Se usa para las claves de escala y traducción.</span><span class="sxs-lookup"><span data-stu-id="fef16-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef16-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fef16-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="fef16-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fef16-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fef16-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="fef16-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="fef16-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fef16-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fef16-113">Marca de tiempo del fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="fef16-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="fef16-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fef16-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="fef16-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="fef16-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fef16-116">[**D3DXVECTOR3**](d3dxvector3.md) vector 3D que proporciona valores de escala y/o de traslación.</span><span class="sxs-lookup"><span data-stu-id="fef16-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fef16-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef16-117">Requirements</span></span>



| <span data-ttu-id="fef16-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef16-118">Requirement</span></span> | <span data-ttu-id="fef16-119">Value</span><span class="sxs-lookup"><span data-stu-id="fef16-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fef16-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fef16-120">Header</span></span><br/> | <dl> <span data-ttu-id="fef16-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef16-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef16-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fef16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef16-123">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="fef16-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
