---
description: La \_ estructura PF FOLLOWSET define los protocolos que pueden preceder o seguir un protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Estructura de PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678063"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="7e09d-103">\_Estructura PF FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="7e09d-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="7e09d-104">La estructura **PF \_ FOLLOWSET** define los protocolos que pueden preceder o seguir un protocolo.</span><span class="sxs-lookup"><span data-stu-id="7e09d-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e09d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e09d-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="7e09d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e09d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e09d-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="7e09d-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="7e09d-108">Número de protocolos de la lista.</span><span class="sxs-lookup"><span data-stu-id="7e09d-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="7e09d-109">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="7e09d-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="7e09d-110">Matriz de estructuras [PF \_ FOLLOWENTRY](pf-followentry.md) que describen cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="7e09d-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e09d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e09d-111">Remarks</span></span>

<span data-ttu-id="7e09d-112">La estructura [PF \_ PARSERINFO](pf-parserinfo.md) utiliza la estructura **PF \_ FOLLOWSET** para enumerar los protocolos que pueden preceder o seguir el protocolo que detecta el analizador.</span><span class="sxs-lookup"><span data-stu-id="7e09d-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="7e09d-113">Monitor de red usa la información de la estructura **PF \_ FOLLOWSET** para actualizar los siguientes conjuntos de analizadores específicos.</span><span class="sxs-lookup"><span data-stu-id="7e09d-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="7e09d-114">La estructura **PF \_ FOLLOWSET** debe estar asignada mediante **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="7e09d-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e09d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e09d-115">Requirements</span></span>



| <span data-ttu-id="7e09d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e09d-116">Requirement</span></span> | <span data-ttu-id="7e09d-117">Value</span><span class="sxs-lookup"><span data-stu-id="7e09d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e09d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e09d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e09d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e09d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7e09d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e09d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e09d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e09d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7e09d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e09d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e09d-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e09d-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e09d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e09d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e09d-125">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="7e09d-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="7e09d-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="7e09d-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 




