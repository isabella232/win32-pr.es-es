---
description: La \_ clase CIM LogicalElement es la clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: CIM_LogicalElement (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907048"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="076c6-103">CIM_LogicalElement (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="076c6-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="076c6-104">La clase **CIM \_ LogicalElement** es la clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="076c6-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="076c6-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="076c6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="076c6-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="076c6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="076c6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="076c6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="076c6-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="076c6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="076c6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="076c6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="076c6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="076c6-110">Members</span></span>

<span data-ttu-id="076c6-111">La clase **CIM \_ LogicalElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="076c6-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="076c6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076c6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="076c6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076c6-113">Properties</span></span>

<span data-ttu-id="076c6-114">La clase **CIM \_ LogicalElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="076c6-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="076c6-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="076c6-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="076c6-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="076c6-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="076c6-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="076c6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="076c6-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="076c6-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="076c6-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="076c6-119">A short textual description of the object.</span></span>

<span data-ttu-id="076c6-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="076c6-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="076c6-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="076c6-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="076c6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="076c6-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="076c6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="076c6-124">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="076c6-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="076c6-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="076c6-125">A textual description of the object.</span></span>

<span data-ttu-id="076c6-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="076c6-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="076c6-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="076c6-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="076c6-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="076c6-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="076c6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="076c6-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="076c6-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="076c6-131">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="076c6-131">Indicates when the object was installed.</span></span> <span data-ttu-id="076c6-132">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="076c6-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="076c6-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="076c6-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="076c6-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="076c6-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="076c6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="076c6-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="076c6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="076c6-137">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="076c6-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="076c6-138">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="076c6-138">Label by which the object is known.</span></span> <span data-ttu-id="076c6-139">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="076c6-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="076c6-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="076c6-141">**Estado**</span><span class="sxs-lookup"><span data-stu-id="076c6-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="076c6-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="076c6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="076c6-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="076c6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="076c6-144">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="076c6-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="076c6-145">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="076c6-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="076c6-146">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="076c6-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="076c6-147">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="076c6-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="076c6-148">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="076c6-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="076c6-149">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="076c6-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="076c6-150">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="076c6-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="076c6-151">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="076c6-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="076c6-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="076c6-153">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="076c6-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="076c6-154">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="076c6-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="076c6-155">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="076c6-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="076c6-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="076c6-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="076c6-157">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="076c6-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="076c6-158">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="076c6-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="076c6-159">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="076c6-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="076c6-160">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="076c6-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="076c6-161">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="076c6-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="076c6-162">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="076c6-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="076c6-163">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="076c6-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="076c6-164">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="076c6-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="076c6-165">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="076c6-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="076c6-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="076c6-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="076c6-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="076c6-167">Remarks</span></span>

<span data-ttu-id="076c6-168">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="076c6-168">WMI does not implement this class.</span></span> <span data-ttu-id="076c6-169">Para las clases derivadas de **CIM \_ LogicalElement**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="076c6-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="076c6-170">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="076c6-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="076c6-171">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="076c6-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="076c6-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076c6-172">Requirements</span></span>



| <span data-ttu-id="076c6-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="076c6-173">Requirement</span></span> | <span data-ttu-id="076c6-174">Value</span><span class="sxs-lookup"><span data-stu-id="076c6-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="076c6-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076c6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="076c6-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="076c6-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="076c6-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076c6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="076c6-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="076c6-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="076c6-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="076c6-179">Namespace</span></span><br/>                | <span data-ttu-id="076c6-180">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="076c6-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="076c6-181">MOF</span><span class="sxs-lookup"><span data-stu-id="076c6-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="076c6-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="076c6-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="076c6-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="076c6-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="076c6-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076c6-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076c6-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="076c6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076c6-186">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="076c6-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

