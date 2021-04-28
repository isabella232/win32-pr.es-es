---
description: 'PageFault_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de error de página. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 clase
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
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106413"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="7ee45-104">Clase PageFault \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="7ee45-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="7ee45-105">Esta clase es la clase de tipo de evento para los eventos de error de página.</span><span class="sxs-lookup"><span data-stu-id="7ee45-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="7ee45-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="7ee45-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee45-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ee45-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="7ee45-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ee45-108">Members</span></span>

<span data-ttu-id="7ee45-109">La **clase PageFault \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ee45-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="7ee45-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ee45-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ee45-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ee45-111">Properties</span></span>

<span data-ttu-id="7ee45-112">La **clase PageFault \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ee45-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ee45-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="7ee45-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ee45-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ee45-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ee45-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ee45-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ee45-116">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="7ee45-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ee45-117">Puntero a la instrucción actual que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="7ee45-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="7ee45-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="7ee45-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ee45-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ee45-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ee45-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ee45-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ee45-121">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="7ee45-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ee45-122">Dirección virtual de la página que produjo el error de la página.</span><span class="sxs-lookup"><span data-stu-id="7ee45-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ee45-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ee45-123">Remarks</span></span>

<span data-ttu-id="7ee45-124">Un error de página se produce cuando una página buscada en la memoria caché no se encuentra allí y se debe recuperar de otra parte de la memoria (un error temporal) o del disco (un error físico).</span><span class="sxs-lookup"><span data-stu-id="7ee45-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee45-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ee45-125">Requirements</span></span>



| <span data-ttu-id="7ee45-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ee45-126">Requirement</span></span> | <span data-ttu-id="7ee45-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7ee45-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ee45-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ee45-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee45-129">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ee45-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ee45-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ee45-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee45-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ee45-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ee45-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ee45-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee45-133">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="7ee45-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




