---
description: La \_ clase de sesión Win32 define la información de estado sobre la interacción entre un usuario y un recurso, como un equipo o una sesión de terminal.
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Win32_Session (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080118"
---
# <a name="win32_session-class"></a><span data-ttu-id="84bb8-103">\_Clase de sesión Win32</span><span class="sxs-lookup"><span data-stu-id="84bb8-103">Win32\_Session class</span></span>

<span data-ttu-id="84bb8-104">La clase de **\_ sesión Win32** define la información de estado sobre la interacción entre un usuario y un recurso, como un equipo o una sesión de terminal.</span><span class="sxs-lookup"><span data-stu-id="84bb8-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="84bb8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="84bb8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="84bb8-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="84bb8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84bb8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84bb8-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="84bb8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="84bb8-108">Members</span></span>

<span data-ttu-id="84bb8-109">La clase de **\_ sesión Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="84bb8-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="84bb8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84bb8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84bb8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84bb8-111">Properties</span></span>

<span data-ttu-id="84bb8-112">La clase de **\_ sesión Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="84bb8-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84bb8-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="84bb8-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84bb8-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="84bb8-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84bb8-117">A short textual description of the object.</span></span>

<span data-ttu-id="84bb8-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84bb8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84bb8-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84bb8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-122">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="84bb8-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-123">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84bb8-123">A textual description of the object.</span></span>

<span data-ttu-id="84bb8-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84bb8-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84bb8-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84bb8-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-128">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="84bb8-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-129">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="84bb8-129">Indicates when the object was installed.</span></span> <span data-ttu-id="84bb8-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="84bb8-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="84bb8-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84bb8-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="84bb8-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84bb8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-135">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="84bb8-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-136">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="84bb8-136">Label by which the object is known.</span></span> <span data-ttu-id="84bb8-137">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="84bb8-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="84bb8-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84bb8-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="84bb8-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84bb8-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-142">Hora a la que se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="84bb8-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="84bb8-143">**Estado**</span><span class="sxs-lookup"><span data-stu-id="84bb8-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bb8-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84bb8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84bb8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84bb8-146">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="84bb8-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84bb8-147">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84bb8-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="84bb8-148">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="84bb8-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="84bb8-149">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="84bb8-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="84bb8-150">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="84bb8-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="84bb8-151">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="84bb8-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="84bb8-152">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="84bb8-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="84bb8-153">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="84bb8-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="84bb8-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84bb8-155">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="84bb8-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84bb8-156">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="84bb8-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84bb8-157">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="84bb8-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84bb8-158">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="84bb8-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84bb8-159">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="84bb8-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84bb8-160">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="84bb8-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84bb8-161">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="84bb8-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84bb8-162">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="84bb8-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84bb8-163">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="84bb8-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84bb8-164">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="84bb8-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84bb8-165">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="84bb8-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84bb8-166">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="84bb8-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84bb8-167">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="84bb8-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="84bb8-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84bb8-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="84bb8-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84bb8-169">Remarks</span></span>

<span data-ttu-id="84bb8-170">La clase de **\_ sesión Win32** se deriva [**de \_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="84bb8-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84bb8-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84bb8-171">Requirements</span></span>



| <span data-ttu-id="84bb8-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="84bb8-172">Requirement</span></span> | <span data-ttu-id="84bb8-173">Value</span><span class="sxs-lookup"><span data-stu-id="84bb8-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84bb8-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84bb8-174">Minimum supported client</span></span><br/> | <span data-ttu-id="84bb8-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84bb8-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84bb8-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84bb8-176">Minimum supported server</span></span><br/> | <span data-ttu-id="84bb8-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84bb8-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84bb8-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84bb8-178">Namespace</span></span><br/>                | <span data-ttu-id="84bb8-179">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="84bb8-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84bb8-180">MOF</span><span class="sxs-lookup"><span data-stu-id="84bb8-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84bb8-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84bb8-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84bb8-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84bb8-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84bb8-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84bb8-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84bb8-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="84bb8-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84bb8-185">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84bb8-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
