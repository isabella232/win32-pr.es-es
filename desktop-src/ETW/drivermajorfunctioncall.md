---
description: Esta clase es la clase de tipo de evento para los eventos de llamada de función principales del controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Clase DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984231"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="f5e55-104">Clase DriverMajorFunctionCall</span><span class="sxs-lookup"><span data-stu-id="f5e55-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="f5e55-105">Esta clase es la clase de tipo de evento para los eventos de llamada de función principales del controlador.</span><span class="sxs-lookup"><span data-stu-id="f5e55-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="f5e55-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="f5e55-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e55-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5e55-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="f5e55-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5e55-108">Members</span></span>

<span data-ttu-id="f5e55-109">La clase **DriverMajorFunctionCall** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f5e55-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="f5e55-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5e55-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5e55-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5e55-111">Properties</span></span>

<span data-ttu-id="f5e55-112">La clase **DriverMajorFunctionCall** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f5e55-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5e55-113">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="f5e55-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-116">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="f5e55-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-117">Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="f5e55-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="f5e55-118">**IRP**</span><span class="sxs-lookup"><span data-stu-id="f5e55-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-121">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="f5e55-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-122">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="f5e55-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="f5e55-123">**MajorFunction**</span><span class="sxs-lookup"><span data-stu-id="f5e55-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-126">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="f5e55-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-127">Código que identifica la función principal a la que se llama.</span><span class="sxs-lookup"><span data-stu-id="f5e55-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="f5e55-128">**MinorFunction**</span><span class="sxs-lookup"><span data-stu-id="f5e55-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-131">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="f5e55-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-132">Código que idenitifies la función secundaria a la que se llama.</span><span class="sxs-lookup"><span data-stu-id="f5e55-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="f5e55-133">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="f5e55-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-136">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="f5e55-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-137">Dirección de la función de controlador que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="f5e55-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="f5e55-138">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="f5e55-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e55-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e55-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5e55-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e55-141">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="f5e55-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="f5e55-142">Identificador que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5e55-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="f5e55-143">Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e55-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5e55-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e55-144">Requirements</span></span>



| <span data-ttu-id="f5e55-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e55-145">Requirement</span></span> | <span data-ttu-id="f5e55-146">Value</span><span class="sxs-lookup"><span data-stu-id="f5e55-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5e55-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5e55-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e55-148">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5e55-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5e55-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5e55-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e55-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5e55-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5e55-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5e55-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e55-152">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="f5e55-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




