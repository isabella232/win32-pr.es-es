---
description: La \_ estructura PF HANDOFFSET define los protocolos que se entregan al analizador, o los protocolos a los que se entrega el analizador.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Estructura de PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667935"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="f0442-103">\_Estructura PF HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="f0442-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="f0442-104">La estructura **PF \_ HANDOFFSET** define los protocolos que se entregan al analizador, o los protocolos a los que se entrega el analizador.</span><span class="sxs-lookup"><span data-stu-id="f0442-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0442-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0442-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="f0442-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0442-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0442-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="f0442-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="f0442-108">Número de protocolos.</span><span class="sxs-lookup"><span data-stu-id="f0442-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="f0442-109">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="f0442-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="f0442-110">Una matriz de estructuras [PF \_ HANDOFFENTRY](pf-handoffentry.md) que definen cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="f0442-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0442-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0442-111">Remarks</span></span>

<span data-ttu-id="f0442-112">La estructura [PF \_ PARSERINFO](pf-parserinfo.md) utiliza la estructura **PF \_ HANDOFFSET** para enumerar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f0442-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="f0442-113">Los protocolos que se entregan al analizador.</span><span class="sxs-lookup"><span data-stu-id="f0442-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="f0442-114">A qué protocolos se entrega el analizador.</span><span class="sxs-lookup"><span data-stu-id="f0442-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="f0442-115">La estructura **PF \_ HANDOFFSET** debe estar asignada mediante **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="f0442-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0442-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0442-116">Requirements</span></span>



| <span data-ttu-id="f0442-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0442-117">Requirement</span></span> | <span data-ttu-id="f0442-118">Value</span><span class="sxs-lookup"><span data-stu-id="f0442-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0442-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0442-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f0442-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f0442-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f0442-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0442-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f0442-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0442-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f0442-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0442-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0442-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0442-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0442-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0442-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0442-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="f0442-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="f0442-127">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="f0442-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 




