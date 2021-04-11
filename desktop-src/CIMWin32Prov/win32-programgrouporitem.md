---
description: La \_ clase WMI abstracta ProgramGroupOrItem de Win32 representa una agrupación lógica de programas en el menú Inicio \\ programas del usuario. Contiene grupos de programas y elementos de grupo de programas.
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Win32_ProgramGroupOrItem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152858"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="6621d-104">\_Clase Win32 ProgramGroupOrItem</span><span class="sxs-lookup"><span data-stu-id="6621d-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="6621d-105">La [clase WMI](../wmisdk/retrieving-a-class.md) abstracta **\_ ProgramGroupOrItem de Win32** representa una agrupación lógica de programas en el menú **Inicio \\ programas** del usuario.</span><span class="sxs-lookup"><span data-stu-id="6621d-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="6621d-106">Contiene grupos de programas y elementos de grupo de programas.</span><span class="sxs-lookup"><span data-stu-id="6621d-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="6621d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6621d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6621d-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6621d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6621d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6621d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="6621d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6621d-110">Members</span></span>

<span data-ttu-id="6621d-111">La **clase \_ ProgramGroupOrItem de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6621d-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="6621d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6621d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6621d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6621d-113">Properties</span></span>

<span data-ttu-id="6621d-114">La **clase \_ ProgramGroupOrItem de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6621d-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6621d-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6621d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6621d-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6621d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6621d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6621d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6621d-118">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6621d-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6621d-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6621d-119">A short textual description of the object.</span></span>

<span data-ttu-id="6621d-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6621d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6621d-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6621d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6621d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6621d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6621d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6621d-124">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="6621d-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6621d-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6621d-125">A textual description of the object.</span></span>

<span data-ttu-id="6621d-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6621d-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6621d-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6621d-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6621d-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6621d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6621d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6621d-130">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="6621d-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6621d-131">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6621d-131">Indicates when the object was installed.</span></span> <span data-ttu-id="6621d-132">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="6621d-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6621d-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6621d-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6621d-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6621d-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6621d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6621d-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6621d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6621d-137">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6621d-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6621d-138">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="6621d-138">Label by which the object is known.</span></span> <span data-ttu-id="6621d-139">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="6621d-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6621d-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6621d-141">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6621d-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6621d-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6621d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6621d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6621d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6621d-144">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="6621d-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6621d-145">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6621d-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="6621d-146">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="6621d-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6621d-147">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="6621d-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6621d-148">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="6621d-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6621d-149">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="6621d-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6621d-150">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="6621d-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6621d-151">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="6621d-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6621d-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6621d-153">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6621d-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6621d-154">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="6621d-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6621d-155">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="6621d-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6621d-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6621d-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6621d-157">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="6621d-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6621d-158">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="6621d-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6621d-159">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="6621d-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6621d-160">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="6621d-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6621d-161">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="6621d-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6621d-162">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="6621d-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6621d-163">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6621d-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6621d-164">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="6621d-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6621d-165">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="6621d-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6621d-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6621d-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6621d-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6621d-167">Remarks</span></span>

<span data-ttu-id="6621d-168">La **clase \_ ProgramGroupOrItem de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6621d-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6621d-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6621d-169">Requirements</span></span>



| <span data-ttu-id="6621d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="6621d-170">Requirement</span></span> | <span data-ttu-id="6621d-171">Value</span><span class="sxs-lookup"><span data-stu-id="6621d-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6621d-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6621d-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6621d-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6621d-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6621d-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6621d-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6621d-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6621d-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6621d-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6621d-176">Namespace</span></span><br/>                | <span data-ttu-id="6621d-177">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6621d-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6621d-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6621d-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6621d-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6621d-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6621d-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6621d-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6621d-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6621d-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6621d-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="6621d-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6621d-183">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6621d-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="6621d-184">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6621d-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
