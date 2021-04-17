---
description: Representa el estado de las características opcionales que están presentes en el sistema operativo.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Clase Win32_OptionalFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659702"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="b841b-103">\_Clase Win32 OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="b841b-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="b841b-104">Representa el estado de las características opcionales que están presentes en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b841b-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="b841b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b841b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b841b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b841b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="b841b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b841b-107">Members</span></span>

<span data-ttu-id="b841b-108">La **clase \_ OptionalFeature de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b841b-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="b841b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b841b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b841b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b841b-110">Properties</span></span>

<span data-ttu-id="b841b-111">La **clase \_ OptionalFeature de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b841b-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b841b-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b841b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b841b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b841b-115">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) (título), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="b841b-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="b841b-116">Un nombre para mostrar de la característica opcional.</span><span class="sxs-lookup"><span data-stu-id="b841b-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="b841b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b841b-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b841b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b841b-120">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b841b-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b841b-121">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b841b-121">A textual description of the object.</span></span>

<span data-ttu-id="b841b-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b841b-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b841b-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b841b-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-124">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b841b-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b841b-126">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b841b-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b841b-127">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b841b-127">Indicates when the object was installed.</span></span> <span data-ttu-id="b841b-128">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b841b-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b841b-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b841b-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b841b-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="b841b-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b841b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b841b-133">Identifica el estado de la característica opcional.</span><span class="sxs-lookup"><span data-stu-id="b841b-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="b841b-134">Los siguientes Estados son posibles:</span><span class="sxs-lookup"><span data-stu-id="b841b-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b841b-135">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="b841b-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b841b-136">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b841b-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="b841b-137">**Ausente** (3)</span><span class="sxs-lookup"><span data-stu-id="b841b-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b841b-138">**Desconocido** (4)</span><span class="sxs-lookup"><span data-stu-id="b841b-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b841b-139">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b841b-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b841b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b841b-142">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) (nombre), [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="b841b-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="b841b-143">Representa el nombre de la característica opcional.</span><span class="sxs-lookup"><span data-stu-id="b841b-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="b841b-144">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b841b-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b841b-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b841b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b841b-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b841b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b841b-147">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b841b-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b841b-148">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b841b-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="b841b-149">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="b841b-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b841b-150">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="b841b-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b841b-151">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="b841b-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b841b-152">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b841b-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b841b-153">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b841b-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b841b-154">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b841b-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b841b-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b841b-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b841b-156">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b841b-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b841b-157">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b841b-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b841b-158">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b841b-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b841b-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b841b-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b841b-160">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b841b-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b841b-161">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b841b-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b841b-162">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b841b-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b841b-163">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b841b-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b841b-164">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b841b-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b841b-165">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b841b-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b841b-166">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b841b-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b841b-167">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b841b-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b841b-168">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b841b-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b841b-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b841b-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b841b-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b841b-170">Requirements</span></span>



| <span data-ttu-id="b841b-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="b841b-171">Requirement</span></span> | <span data-ttu-id="b841b-172">Value</span><span class="sxs-lookup"><span data-stu-id="b841b-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b841b-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b841b-173">Minimum supported client</span></span><br/> | <span data-ttu-id="b841b-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b841b-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b841b-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b841b-175">Minimum supported server</span></span><br/> | <span data-ttu-id="b841b-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b841b-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b841b-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b841b-177">Namespace</span></span><br/>                | <span data-ttu-id="b841b-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b841b-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b841b-179">MOF</span><span class="sxs-lookup"><span data-stu-id="b841b-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b841b-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b841b-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b841b-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b841b-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b841b-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b841b-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b841b-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="b841b-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b841b-184">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b841b-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="b841b-185">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b841b-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="b841b-186">Consultar el estado de las características opcionales</span><span class="sxs-lookup"><span data-stu-id="b841b-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
