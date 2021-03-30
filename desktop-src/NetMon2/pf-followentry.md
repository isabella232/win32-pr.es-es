---
description: La \_ estructura PF FOLLOWENTRY define un protocolo que monitor de red agrega al siguiente conjunto de un analizador.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Estructura de PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910881"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="d0b41-103">\_Estructura PF FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="d0b41-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="d0b41-104">La estructura **PF \_ FOLLOWENTRY** define un protocolo que monitor de red agrega al siguiente conjunto de un analizador.</span><span class="sxs-lookup"><span data-stu-id="d0b41-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b41-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="d0b41-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0b41-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0b41-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="d0b41-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d0b41-108">El nombre del protocolo</span><span class="sxs-lookup"><span data-stu-id="d0b41-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0b41-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0b41-109">Remarks</span></span>

<span data-ttu-id="d0b41-110">La estructura [PF \_ FOLLOWSET](pf-followset.md) usa una matriz de estructuras **PF \_ FOLLOWENTRY** .</span><span class="sxs-lookup"><span data-stu-id="d0b41-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b41-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b41-111">Requirements</span></span>



| <span data-ttu-id="d0b41-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b41-112">Requirement</span></span> | <span data-ttu-id="d0b41-113">Value</span><span class="sxs-lookup"><span data-stu-id="d0b41-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b41-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b41-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b41-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0b41-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0b41-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b41-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b41-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0b41-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0b41-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0b41-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b41-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b41-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b41-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b41-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b41-121">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="d0b41-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




