---
description: La \_ clase CIM SystemResource representa una entidad administrada por BIOS o un sistema operativo que está disponible para su uso por software y dispositivos lógicos.
ms.assetid: f232c940-532d-4723-8e1e-09f983664b84
ms.tgt_platform: multiple
title: CIM_SystemResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemResource
- CIM_SystemResource.Caption
- CIM_SystemResource.Description
- CIM_SystemResource.InstallDate
- CIM_SystemResource.Name
- CIM_SystemResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0c111aa0d69119a7d9182732fb18dd5109d3dde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275014"
---
# <a name="cim_systemresource-class"></a><span data-ttu-id="9ee5f-103">\_Clase SystemResource de CIM</span><span class="sxs-lookup"><span data-stu-id="9ee5f-103">CIM\_SystemResource class</span></span>

<span data-ttu-id="9ee5f-104">La clase **CIM \_ SystemResource** representa una entidad administrada por BIOS o un sistema operativo que está disponible para su uso por software y dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-104">The **CIM\_SystemResource** class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ee5f-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ee5f-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ee5f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9ee5f-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee5f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ee5f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C519-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SystemResource : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="9ee5f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ee5f-110">Members</span></span>

<span data-ttu-id="9ee5f-111">La clase **CIM \_ SystemResource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9ee5f-111">The **CIM\_SystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="9ee5f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ee5f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ee5f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ee5f-113">Properties</span></span>

<span data-ttu-id="9ee5f-114">La clase **CIM \_ SystemResource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-114">The **CIM\_SystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ee5f-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee5f-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ee5f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ee5f-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-119">A short textual description of the object.</span></span>

<span data-ttu-id="9ee5f-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee5f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee5f-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ee5f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-124">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ee5f-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-125">A textual description of the object.</span></span>

<span data-ttu-id="9ee5f-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee5f-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee5f-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ee5f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ee5f-131">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-131">Indicates when the object was installed.</span></span> <span data-ttu-id="9ee5f-132">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9ee5f-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee5f-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee5f-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ee5f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-137">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee5f-138">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-138">Label by which the object is known.</span></span> <span data-ttu-id="9ee5f-139">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9ee5f-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee5f-141">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee5f-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ee5f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee5f-144">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ee5f-145">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="9ee5f-146">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9ee5f-147">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="9ee5f-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9ee5f-148">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9ee5f-149">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="9ee5f-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9ee5f-150">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9ee5f-151">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9ee5f-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ee5f-153">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ee5f-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ee5f-154">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ee5f-155">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ee5f-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ee5f-157">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ee5f-158">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ee5f-159">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ee5f-160">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ee5f-161">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ee5f-162">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ee5f-163">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ee5f-164">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ee5f-165">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9ee5f-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9ee5f-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9ee5f-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9ee5f-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ee5f-167">Remarks</span></span>

<span data-ttu-id="9ee5f-168">La clase **CIM \_ SystemResource** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-168">The **CIM\_SystemResource** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="9ee5f-169">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-169">WMI does not implement this class.</span></span> <span data-ttu-id="9ee5f-170">Para las clases WMI derivadas de **CIM \_ SystemResource**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5f-170">For WMI classes derived from **CIM\_SystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ee5f-171">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ee5f-172">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9ee5f-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee5f-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ee5f-173">Requirements</span></span>



| <span data-ttu-id="9ee5f-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ee5f-174">Requirement</span></span> | <span data-ttu-id="9ee5f-175">Value</span><span class="sxs-lookup"><span data-stu-id="9ee5f-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee5f-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ee5f-176">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee5f-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ee5f-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ee5f-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ee5f-178">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee5f-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ee5f-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ee5f-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ee5f-180">Namespace</span></span><br/>                | <span data-ttu-id="9ee5f-181">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9ee5f-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ee5f-182">MOF</span><span class="sxs-lookup"><span data-stu-id="9ee5f-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ee5f-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ee5f-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ee5f-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ee5f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ee5f-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee5f-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee5f-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ee5f-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee5f-187">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9ee5f-187">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

