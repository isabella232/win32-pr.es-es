---
description: La \_ clase del ManagedSystemElement de CIM es la clase base para la jerarquía de elementos del sistema. Cualquier componente del sistema distinguible es un candidato para la inclusión en esta clase.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: CIM_ManagedSystemElement (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153159"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="7b05c-104">CIM_ManagedSystemElement (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7b05c-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7b05c-105">La clase del **\_ ManagedSystemElement de CIM** es la clase base para la jerarquía de elementos del sistema.</span><span class="sxs-lookup"><span data-stu-id="7b05c-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="7b05c-106">Cualquier componente del sistema distinguible es un candidato para la inclusión en esta clase.</span><span class="sxs-lookup"><span data-stu-id="7b05c-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="7b05c-107">Algunos ejemplos son componentes de software, como archivos; dispositivos, como unidades de disco y controladores; y componentes físicos, como chips y tarjetas.</span><span class="sxs-lookup"><span data-stu-id="7b05c-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b05c-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7b05c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b05c-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b05c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b05c-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7b05c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b05c-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7b05c-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b05c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b05c-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="7b05c-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b05c-113">Members</span></span>

<span data-ttu-id="7b05c-114">La clase del **\_ ManagedSystemElement de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b05c-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="7b05c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b05c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b05c-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b05c-116">Properties</span></span>

<span data-ttu-id="7b05c-117">La clase del **\_ ManagedSystemElement de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7b05c-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b05c-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7b05c-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b05c-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b05c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b05c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7b05c-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7b05c-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7b05c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b05c-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b05c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b05c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b05c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-126">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7b05c-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7b05c-127">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7b05c-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b05c-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b05c-129">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b05c-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b05c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7b05c-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7b05c-132">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-132">Indicates when the object was installed.</span></span> <span data-ttu-id="7b05c-133">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7b05c-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="7b05c-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7b05c-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b05c-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b05c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b05c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-137">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7b05c-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7b05c-138">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-138">Label by which the object is known.</span></span> <span data-ttu-id="7b05c-139">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7b05c-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="7b05c-140">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7b05c-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b05c-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b05c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b05c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b05c-143">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7b05c-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7b05c-144">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="7b05c-145">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7b05c-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7b05c-146">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7b05c-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7b05c-147">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7b05c-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7b05c-148">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7b05c-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7b05c-149">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7b05c-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7b05c-150">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7b05c-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7b05c-151">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b05c-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7b05c-152">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7b05c-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7b05c-153">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7b05c-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b05c-154">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7b05c-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b05c-155">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7b05c-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7b05c-156">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7b05c-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7b05c-157">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7b05c-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7b05c-158">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7b05c-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7b05c-159">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7b05c-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7b05c-160">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7b05c-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7b05c-161">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7b05c-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7b05c-162">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7b05c-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7b05c-163">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7b05c-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7b05c-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7b05c-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7b05c-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b05c-165">Remarks</span></span>

<span data-ttu-id="7b05c-166">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7b05c-166">WMI does not implement this class.</span></span> <span data-ttu-id="7b05c-167">Para las clases WMI derivadas de esta clase, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7b05c-168">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b05c-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b05c-169">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7b05c-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b05c-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b05c-170">Requirements</span></span>



| <span data-ttu-id="7b05c-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b05c-171">Requirement</span></span> | <span data-ttu-id="7b05c-172">Value</span><span class="sxs-lookup"><span data-stu-id="7b05c-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b05c-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b05c-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7b05c-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b05c-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b05c-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b05c-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7b05c-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b05c-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b05c-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b05c-177">Namespace</span></span><br/>                | <span data-ttu-id="7b05c-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7b05c-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b05c-179">MOF</span><span class="sxs-lookup"><span data-stu-id="7b05c-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b05c-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b05c-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b05c-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b05c-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b05c-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b05c-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

