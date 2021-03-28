---
description: Esta clase es la clase de tipo de evento para los eventos de llamada a procedimiento diferido (DPC) del dispositivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Clase DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907710"
---
# <a name="dpc-class"></a><span data-ttu-id="0e1f8-104">Clase DPC</span><span class="sxs-lookup"><span data-stu-id="0e1f8-104">DPC class</span></span>

<span data-ttu-id="0e1f8-105">Esta clase es la clase de tipo de evento para los eventos de llamada a procedimiento diferido (DPC) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="0e1f8-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e1f8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e1f8-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="0e1f8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e1f8-108">Members</span></span>

<span data-ttu-id="0e1f8-109">La clase **DPC** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0e1f8-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="0e1f8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e1f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e1f8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e1f8-111">Properties</span></span>

<span data-ttu-id="0e1f8-112">La clase **DPC** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e1f8-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="0e1f8-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e1f8-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0e1f8-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0e1f8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e1f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e1f8-116">Calificadores: WmiDataId (1), extensión ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="0e1f8-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="0e1f8-117">Hora de entrada de DPC.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="0e1f8-118">**Rutina**</span><span class="sxs-lookup"><span data-stu-id="0e1f8-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e1f8-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e1f8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e1f8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e1f8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e1f8-121">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="0e1f8-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0e1f8-122">Dirección de la rutina de DPC.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-122">Address of DPC routine.</span></span> <span data-ttu-id="0e1f8-123">Use la dirección con los eventos de imagen para buscar la imagen que se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e1f8-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e1f8-124">Remarks</span></span>

<span data-ttu-id="0e1f8-125">Estos eventos se registran cuando se introduce un DPC.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="0e1f8-126">Estos eventos se usan para supervisar y comprobar el comportamiento de los controladores y los componentes de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="0e1f8-127">Por ejemplo, puede usar los eventos DPC, ISR y imagen para determinar los componentes que emplean demasiado tiempo en los niveles de interrupción altos.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="0e1f8-128">Los eventos de DPC y ISR tienen una marca de tiempo de entrada que se utiliza para calcular la duración de las rutinas.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="0e1f8-129">Los eventos de imagen se leen para construir las regiones de memoria que se asignan a determinados módulos.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="0e1f8-130">Puede usar la asignación para buscar el módulo que contiene la rutina de interrupción.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="0e1f8-131">El evento TimerDPC se registra cuando un DPC se desencadena como resultado de una expiración del temporizador y el evento ThreadDPC se registra cuando se ejecuta un DPC enlazado.</span><span class="sxs-lookup"><span data-stu-id="0e1f8-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e1f8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e1f8-132">Requirements</span></span>



| <span data-ttu-id="0e1f8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e1f8-133">Requirement</span></span> | <span data-ttu-id="0e1f8-134">Value</span><span class="sxs-lookup"><span data-stu-id="0e1f8-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e1f8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e1f8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0e1f8-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e1f8-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e1f8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e1f8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0e1f8-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e1f8-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




