---
description: Representa el encabezado común que usan todas las clases MSMCAEvent. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697474"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="3681d-104">\_Clase de encabezado MSMCAEvent</span><span class="sxs-lookup"><span data-stu-id="3681d-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="3681d-105">La clase de **\_ encabezado MSMCAEvent** representa el encabezado común que usan todas [las clases MSMCA](msmca-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="3681d-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="3681d-106">Los archivos de encabezado se usan para que el código de C y C++ pueda tener una estructura de datos que describa el encabezado común para todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="3681d-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="3681d-107">Esta clase está reservada para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3681d-107">This class is reserved for internal use.</span></span> <span data-ttu-id="3681d-108">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3681d-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="3681d-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3681d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3681d-110">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3681d-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3681d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3681d-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="3681d-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="3681d-112">Members</span></span>

<span data-ttu-id="3681d-113">La clase de **\_ encabezado MSMCAEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3681d-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="3681d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3681d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3681d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3681d-115">Properties</span></span>

<span data-ttu-id="3681d-116">La clase de **\_ encabezado MSMCAEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3681d-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3681d-117">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="3681d-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3681d-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-120">Número de errores adicionales en el registro de MCA.</span><span class="sxs-lookup"><span data-stu-id="3681d-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="3681d-121">**CPU**</span><span class="sxs-lookup"><span data-stu-id="3681d-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3681d-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-124">CPU que informa del error.</span><span class="sxs-lookup"><span data-stu-id="3681d-124">CPU that reports the error.</span></span> <span data-ttu-id="3681d-125">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3681d-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3681d-126">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="3681d-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-127">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3681d-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-129">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="3681d-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="3681d-130">Value</span><span class="sxs-lookup"><span data-stu-id="3681d-130">Value</span></span>                                                                                                | <span data-ttu-id="3681d-131">Significado</span><span class="sxs-lookup"><span data-stu-id="3681d-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3681d-132"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="3681d-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3681d-133">Recuperable</span><span class="sxs-lookup"><span data-stu-id="3681d-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="3681d-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3681d-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3681d-135">Crítico</span><span class="sxs-lookup"><span data-stu-id="3681d-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="3681d-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3681d-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3681d-137">Corregible</span><span class="sxs-lookup"><span data-stu-id="3681d-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3681d-138">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="3681d-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3681d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-141">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3681d-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="3681d-142">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="3681d-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3681d-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-145">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="3681d-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="3681d-146">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3681d-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3681d-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3681d-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3681d-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3681d-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3681d-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3681d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3681d-150">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="3681d-150">Type of event log message.</span></span> <span data-ttu-id="3681d-151">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="3681d-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3681d-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3681d-152">Requirements</span></span>



| <span data-ttu-id="3681d-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="3681d-153">Requirement</span></span> | <span data-ttu-id="3681d-154">Value</span><span class="sxs-lookup"><span data-stu-id="3681d-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3681d-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3681d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3681d-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3681d-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3681d-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3681d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3681d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3681d-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3681d-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3681d-159">Namespace</span></span><br/>                | <span data-ttu-id="3681d-160">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="3681d-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3681d-161">MOF</span><span class="sxs-lookup"><span data-stu-id="3681d-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3681d-162"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3681d-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3681d-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3681d-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3681d-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3681d-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3681d-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="3681d-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3681d-166">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="3681d-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="3681d-167">Clases de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="3681d-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

