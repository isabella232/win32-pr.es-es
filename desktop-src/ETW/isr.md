---
description: Esta clase es la clase de tipo de evento para los eventos de la rutina de servicio de interrupción (ISR). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985598"
---
# <a name="isr-class"></a><span data-ttu-id="5c5f7-104">ISR (clase)</span><span class="sxs-lookup"><span data-stu-id="5c5f7-104">ISR class</span></span>

<span data-ttu-id="5c5f7-105">Esta clase es la clase de tipo de evento para los eventos de la rutina de servicio de interrupción (ISR).</span><span class="sxs-lookup"><span data-stu-id="5c5f7-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="5c5f7-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5f7-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="5c5f7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c5f7-108">Members</span></span>

<span data-ttu-id="5c5f7-109">La clase **ISR** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c5f7-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="5c5f7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c5f7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c5f7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c5f7-111">Properties</span></span>

<span data-ttu-id="5c5f7-112">La clase **ISR** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c5f7-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f7-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5f7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-116">Calificadores: WmiDataId (1), extensión ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="5c5f7-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f7-117">Hora de entrada de ISR.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="5c5f7-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f7-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5f7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-121">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="5c5f7-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5c5f7-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c5f7-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f7-124">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5f7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-126">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5c5f7-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5c5f7-127">Valor booleano que indica si se ha reclamado la interrupción (es true si se ha reclamado la interrupción).</span><span class="sxs-lookup"><span data-stu-id="5c5f7-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f7-128">**Rutina**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f7-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5f7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-131">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="5c5f7-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5c5f7-132">Dirección de la rutina de ISR.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-132">Address of ISR routine.</span></span> <span data-ttu-id="5c5f7-133">Use la dirección con los eventos de imagen para buscar la imagen que se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="5c5f7-134">**Vector**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f7-135">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5c5f7-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5f7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f7-137">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="5c5f7-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5c5f7-138">Vector de la tabla de descriptores de interrupción a la que se asigna la rutina de ISR.</span><span class="sxs-lookup"><span data-stu-id="5c5f7-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c5f7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c5f7-139">Requirements</span></span>



| <span data-ttu-id="5c5f7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5f7-140">Requirement</span></span> | <span data-ttu-id="5c5f7-141">Value</span><span class="sxs-lookup"><span data-stu-id="5c5f7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c5f7-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c5f7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5f7-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5c5f7-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c5f7-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c5f7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5f7-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c5f7-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




