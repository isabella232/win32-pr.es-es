---
description: Describe una función utilizada por un efecto.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: D3DXFUNCTION_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698246"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="e9dc1-103">D3DXFUNCTION \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="e9dc1-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="e9dc1-104">Describe una función utilizada por un efecto.</span><span class="sxs-lookup"><span data-stu-id="e9dc1-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9dc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9dc1-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="e9dc1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9dc1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9dc1-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e9dc1-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e9dc1-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9dc1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e9dc1-109">Nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="e9dc1-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="e9dc1-110">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="e9dc1-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="e9dc1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9dc1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e9dc1-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e9dc1-112">Unused.</span></span> <span data-ttu-id="e9dc1-113">Este miembro siempre se establecerá en cero por [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span><span class="sxs-lookup"><span data-stu-id="e9dc1-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9dc1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9dc1-114">Requirements</span></span>



| <span data-ttu-id="e9dc1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9dc1-115">Requirement</span></span> | <span data-ttu-id="e9dc1-116">Value</span><span class="sxs-lookup"><span data-stu-id="e9dc1-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dc1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9dc1-117">Header</span></span><br/> | <dl> <span data-ttu-id="e9dc1-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc1-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9dc1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9dc1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dc1-120">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="e9dc1-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
