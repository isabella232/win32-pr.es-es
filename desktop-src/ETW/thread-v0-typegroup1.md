---
description: Esta clase es la clase de tipo de evento para eventos de subproceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Thread_V0_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984771"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="a7dbe-104">Thread \_ V0 \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="a7dbe-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="a7dbe-105">Esta clase es la clase de tipo de evento para eventos de subproceso.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="a7dbe-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7dbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7dbe-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="a7dbe-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7dbe-108">Members</span></span>

<span data-ttu-id="a7dbe-109">La clase **Thread \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a7dbe-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a7dbe-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7dbe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7dbe-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7dbe-111">Properties</span></span>

<span data-ttu-id="a7dbe-112">La clase **Thread \_ V0 \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7dbe-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="a7dbe-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7dbe-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7dbe-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7dbe-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7dbe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7dbe-116">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a7dbe-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a7dbe-117">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="a7dbe-118">TThreadId</span><span class="sxs-lookup"><span data-stu-id="a7dbe-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7dbe-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7dbe-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7dbe-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7dbe-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7dbe-121">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a7dbe-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a7dbe-122">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7dbe-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7dbe-123">Requirements</span></span>



| <span data-ttu-id="a7dbe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7dbe-124">Requirement</span></span> | <span data-ttu-id="a7dbe-125">Value</span><span class="sxs-lookup"><span data-stu-id="a7dbe-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a7dbe-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7dbe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7dbe-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a7dbe-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a7dbe-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7dbe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7dbe-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7dbe-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a7dbe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7dbe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7dbe-131">**Subproceso \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a7dbe-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




