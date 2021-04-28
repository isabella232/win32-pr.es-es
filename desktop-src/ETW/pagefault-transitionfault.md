---
description: 'PageFault_TransitionFault clase : esta clase es la clase de tipo de evento para los eventos de error de página. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106463"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="53fda-104">PageFault \_ TransitionFault (clase)</span><span class="sxs-lookup"><span data-stu-id="53fda-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="53fda-105">Esta clase es la clase de tipo de evento para los eventos de error de página.</span><span class="sxs-lookup"><span data-stu-id="53fda-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="53fda-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="53fda-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fda-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53fda-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="53fda-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="53fda-108">Members</span></span>

<span data-ttu-id="53fda-109">La **clase PageFault \_ TransitionFault** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="53fda-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="53fda-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53fda-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53fda-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53fda-111">Properties</span></span>

<span data-ttu-id="53fda-112">La **clase PageFault \_ TransitionFault** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="53fda-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53fda-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="53fda-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53fda-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="53fda-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53fda-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53fda-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53fda-116">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="53fda-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="53fda-117">Puntero a la instrucción actual que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="53fda-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="53fda-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="53fda-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53fda-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="53fda-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53fda-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53fda-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53fda-121">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="53fda-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="53fda-122">Dirección virtual de la página que produjo el error de la página.</span><span class="sxs-lookup"><span data-stu-id="53fda-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53fda-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53fda-123">Requirements</span></span>



| <span data-ttu-id="53fda-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53fda-124">Requirement</span></span> | <span data-ttu-id="53fda-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53fda-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="53fda-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53fda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53fda-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53fda-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="53fda-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53fda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53fda-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53fda-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="53fda-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53fda-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fda-131">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="53fda-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




