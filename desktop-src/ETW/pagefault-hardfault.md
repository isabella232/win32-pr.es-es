---
description: Esta clase es la clase de tipo de evento para los eventos de error de página de hardware. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002288"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="d06bd-104">Errores \_ HardFault (clase)</span><span class="sxs-lookup"><span data-stu-id="d06bd-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="d06bd-105">Esta clase es la clase de tipo de evento para los eventos de error de página de hardware.</span><span class="sxs-lookup"><span data-stu-id="d06bd-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="d06bd-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d06bd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d06bd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d06bd-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="d06bd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d06bd-108">Members</span></span>

<span data-ttu-id="d06bd-109">La clase **errores \_ HardFault** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d06bd-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="d06bd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d06bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d06bd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d06bd-111">Properties</span></span>

<span data-ttu-id="d06bd-112">La clase **errores \_ HardFault** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d06bd-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d06bd-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="d06bd-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d06bd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-116">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="d06bd-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-117">Cantidad de datos leídos de ReadOffset para satisfacer el error.</span><span class="sxs-lookup"><span data-stu-id="d06bd-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="d06bd-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="d06bd-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d06bd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-121">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="d06bd-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-122">Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento de [**\_ nombre FileIo**](fileio-name.md) para determinar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="d06bd-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="d06bd-123">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="d06bd-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d06bd-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-126">Calificadores: WmiDataId (1), extensión ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="d06bd-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-127">Marca de hora de inicio en la que se produjo el error de página.</span><span class="sxs-lookup"><span data-stu-id="d06bd-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d06bd-128">**ReadOffset**</span><span class="sxs-lookup"><span data-stu-id="d06bd-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d06bd-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-131">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="d06bd-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-132">Desplazamiento de archivo desde el que se leyeron los datos para satisfacer el error.</span><span class="sxs-lookup"><span data-stu-id="d06bd-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="d06bd-133">**TThreadId**</span><span class="sxs-lookup"><span data-stu-id="d06bd-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d06bd-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-136">Calificadores: WmiDataId (5), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="d06bd-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-137">Identificador de subproceso del subproceso que encontró el error de página.</span><span class="sxs-lookup"><span data-stu-id="d06bd-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="d06bd-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="d06bd-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d06bd-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d06bd-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d06bd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d06bd-141">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="d06bd-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d06bd-142">Dirección de error.</span><span class="sxs-lookup"><span data-stu-id="d06bd-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d06bd-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d06bd-143">Requirements</span></span>



| <span data-ttu-id="d06bd-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d06bd-144">Requirement</span></span> | <span data-ttu-id="d06bd-145">Value</span><span class="sxs-lookup"><span data-stu-id="d06bd-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d06bd-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d06bd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d06bd-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d06bd-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d06bd-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d06bd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d06bd-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d06bd-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d06bd-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d06bd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06bd-151">**Errores \_ V2**</span><span class="sxs-lookup"><span data-stu-id="d06bd-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




