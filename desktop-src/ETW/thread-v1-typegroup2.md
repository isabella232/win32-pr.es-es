---
description: Esta clase es la clase de tipo de evento para los eventos de fin de subproceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543078"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="7eee7-104">\_ \_ Clase TypeGroup2 de Thread v1</span><span class="sxs-lookup"><span data-stu-id="7eee7-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="7eee7-105">Esta clase es la clase de tipo de evento para los eventos de fin de subproceso.</span><span class="sxs-lookup"><span data-stu-id="7eee7-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="7eee7-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7eee7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eee7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eee7-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="7eee7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eee7-108">Members</span></span>

<span data-ttu-id="7eee7-109">La **clase \_ \_ TypeGroup2 del subproceso v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7eee7-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="7eee7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7eee7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eee7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7eee7-111">Properties</span></span>

<span data-ttu-id="7eee7-112">La **clase \_ \_ TypeGroup2 del subproceso v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7eee7-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eee7-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="7eee7-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eee7-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eee7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eee7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eee7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eee7-116">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="7eee7-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7eee7-117">Identificador de proceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="7eee7-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="7eee7-118">**Windows Server 2003:** Contiene el calificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="7eee7-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="7eee7-119">TThreadId</span><span class="sxs-lookup"><span data-stu-id="7eee7-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eee7-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eee7-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eee7-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7eee7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eee7-122">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7eee7-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7eee7-123">Identificador de subproceso del subproceso implicado en el evento.</span><span class="sxs-lookup"><span data-stu-id="7eee7-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="7eee7-124">**Windows Server 2003:** Contiene el calificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="7eee7-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7eee7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eee7-125">Requirements</span></span>



| <span data-ttu-id="7eee7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eee7-126">Requirement</span></span> | <span data-ttu-id="7eee7-127">Value</span><span class="sxs-lookup"><span data-stu-id="7eee7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7eee7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eee7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7eee7-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7eee7-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7eee7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eee7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7eee7-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7eee7-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7eee7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eee7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eee7-133">**Subproceso \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7eee7-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




