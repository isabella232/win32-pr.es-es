---
description: Esta clase es la clase de tipo de evento para los eventos de solicitud de finalización de controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Clase DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984235"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="5e9ce-104">Clase DriverCompleteRequest</span><span class="sxs-lookup"><span data-stu-id="5e9ce-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="5e9ce-105">Esta clase es la clase de tipo de evento para los eventos de solicitud de finalización de controlador.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="5e9ce-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e9ce-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="5e9ce-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e9ce-108">Members</span></span>

<span data-ttu-id="5e9ce-109">La clase **DriverCompleteRequest** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e9ce-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="5e9ce-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e9ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e9ce-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e9ce-111">Properties</span></span>

<span data-ttu-id="5e9ce-112">La clase **DriverCompleteRequest** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e9ce-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e9ce-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e9ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-116">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="5e9ce-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e9ce-117">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="5e9ce-118">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e9ce-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e9ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="5e9ce-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e9ce-122">Dirección de la función de controlador que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="5e9ce-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e9ce-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e9ce-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e9ce-126">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5e9ce-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5e9ce-127">Identificador que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e9ce-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="5e9ce-128">Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .</span><span class="sxs-lookup"><span data-stu-id="5e9ce-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e9ce-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9ce-129">Requirements</span></span>



| <span data-ttu-id="5e9ce-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9ce-130">Requirement</span></span> | <span data-ttu-id="5e9ce-131">Value</span><span class="sxs-lookup"><span data-stu-id="5e9ce-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e9ce-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9ce-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9ce-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e9ce-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9ce-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9ce-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e9ce-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e9ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9ce-137">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="5e9ce-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




