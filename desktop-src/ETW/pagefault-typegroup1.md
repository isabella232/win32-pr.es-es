---
description: Esta clase es la clase de tipo de evento para los eventos de error de página. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277579"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="f152f-104">Errores \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="f152f-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="f152f-105">Esta clase es la clase de tipo de evento para los eventos de error de página.</span><span class="sxs-lookup"><span data-stu-id="f152f-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="f152f-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="f152f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f152f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f152f-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="f152f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f152f-108">Members</span></span>

<span data-ttu-id="f152f-109">La clase **errores \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f152f-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f152f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f152f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f152f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f152f-111">Properties</span></span>

<span data-ttu-id="f152f-112">La clase **errores \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f152f-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f152f-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="f152f-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f152f-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f152f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f152f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f152f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f152f-116">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="f152f-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f152f-117">Puntero a la instrucción actual que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f152f-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="f152f-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="f152f-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f152f-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f152f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f152f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f152f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f152f-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="f152f-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f152f-122">Dirección virtual de la página que causó el error de página.</span><span class="sxs-lookup"><span data-stu-id="f152f-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f152f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f152f-123">Remarks</span></span>

<span data-ttu-id="f152f-124">Se produce un error de página cuando no se encuentra una página que se busca en la memoria caché y debe recuperarse de otro lugar de la memoria (un error de software) o del disco (un error de hardware).</span><span class="sxs-lookup"><span data-stu-id="f152f-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="f152f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f152f-125">Requirements</span></span>



| <span data-ttu-id="f152f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f152f-126">Requirement</span></span> | <span data-ttu-id="f152f-127">Value</span><span class="sxs-lookup"><span data-stu-id="f152f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f152f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f152f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f152f-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f152f-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f152f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f152f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f152f-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f152f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f152f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f152f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f152f-133">**Errores \_ V2**</span><span class="sxs-lookup"><span data-stu-id="f152f-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




