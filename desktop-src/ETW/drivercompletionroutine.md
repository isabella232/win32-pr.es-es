---
description: Esta clase es la clase de tipo de evento para eventos de rutina completa de controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Clase DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907709"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="1da44-104">Clase DriverCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1da44-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="1da44-105">Esta clase es la clase de tipo de evento para eventos de rutina completa de controlador.</span><span class="sxs-lookup"><span data-stu-id="1da44-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="1da44-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="1da44-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da44-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1da44-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="1da44-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1da44-108">Members</span></span>

<span data-ttu-id="1da44-109">La clase **DriverCompletionRoutine** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1da44-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="1da44-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1da44-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1da44-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1da44-111">Properties</span></span>

<span data-ttu-id="1da44-112">La clase **DriverCompletionRoutine** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1da44-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1da44-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="1da44-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da44-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1da44-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da44-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1da44-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1da44-116">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="1da44-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1da44-117">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="1da44-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="1da44-118">**Rutina**</span><span class="sxs-lookup"><span data-stu-id="1da44-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da44-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1da44-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da44-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1da44-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1da44-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="1da44-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1da44-122">Dirección de la función de controlador que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="1da44-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="1da44-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="1da44-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da44-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1da44-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da44-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1da44-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1da44-126">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="1da44-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="1da44-127">Identificador que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1da44-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="1da44-128">Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="1da44-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1da44-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1da44-129">Requirements</span></span>



| <span data-ttu-id="1da44-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1da44-130">Requirement</span></span> | <span data-ttu-id="1da44-131">Value</span><span class="sxs-lookup"><span data-stu-id="1da44-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1da44-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1da44-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1da44-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1da44-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1da44-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1da44-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1da44-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1da44-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1da44-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1da44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da44-137">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="1da44-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




