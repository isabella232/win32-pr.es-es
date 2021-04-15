---
description: Describe una clave de devolución de llamada para su uso en la animación de fotogramas clave.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: D3DXKEY_CALLBACK estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707876"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="b09c9-103">D3DXKEY ( \_ estructura de devolución de llamada)</span><span class="sxs-lookup"><span data-stu-id="b09c9-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="b09c9-104">Describe una clave de devolución de llamada para su uso en la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="b09c9-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b09c9-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="b09c9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b09c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b09c9-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="b09c9-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="b09c9-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b09c9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b09c9-109">Marca de tiempo del fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="b09c9-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="b09c9-110">**pCallbackData**</span><span class="sxs-lookup"><span data-stu-id="b09c9-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="b09c9-111">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b09c9-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b09c9-112">Puntero a los datos de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="b09c9-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b09c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b09c9-113">Requirements</span></span>



| <span data-ttu-id="b09c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b09c9-114">Requirement</span></span> | <span data-ttu-id="b09c9-115">Value</span><span class="sxs-lookup"><span data-stu-id="b09c9-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b09c9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b09c9-116">Header</span></span><br/> | <dl> <span data-ttu-id="b09c9-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b09c9-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09c9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b09c9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09c9-119">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="b09c9-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
