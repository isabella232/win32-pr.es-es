---
description: La \_ clase WMI ClassicCOMClass de Win32 representa las propiedades de un componente com.
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Win32_ClassicCOMClass (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659680"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="79657-103">\_Clase Win32 ClassicCOMClass</span><span class="sxs-lookup"><span data-stu-id="79657-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="79657-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClass de Win32** representa las propiedades de un componente com.</span><span class="sxs-lookup"><span data-stu-id="79657-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="79657-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="79657-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="79657-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="79657-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79657-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79657-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="79657-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="79657-108">Members</span></span>

<span data-ttu-id="79657-109">La **clase \_ ClassicCOMClass de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79657-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="79657-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79657-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79657-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79657-111">Properties</span></span>

<span data-ttu-id="79657-112">La **clase \_ ClassicCOMClass de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79657-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79657-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="79657-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79657-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79657-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="79657-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="79657-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79657-117">A short textual description of the object.</span></span>

<span data-ttu-id="79657-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79657-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79657-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="79657-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79657-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79657-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-122">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="79657-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="79657-123">Identificador único global (GUID) de esta clase COM.</span><span class="sxs-lookup"><span data-stu-id="79657-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="79657-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79657-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79657-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79657-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-127">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="79657-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="79657-128">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79657-128">A textual description of the object.</span></span>

<span data-ttu-id="79657-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79657-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79657-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79657-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79657-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79657-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-133">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="79657-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="79657-134">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="79657-134">Indicates when the object was installed.</span></span> <span data-ttu-id="79657-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="79657-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="79657-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79657-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79657-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="79657-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79657-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79657-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-140">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="79657-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="79657-141">La propiedad Name contiene el nombre legible para la clase COM.</span><span class="sxs-lookup"><span data-stu-id="79657-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="79657-142">**Estado**</span><span class="sxs-lookup"><span data-stu-id="79657-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79657-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79657-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79657-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79657-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79657-145">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="79657-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="79657-146">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79657-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="79657-147">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="79657-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="79657-148">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="79657-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="79657-149">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="79657-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="79657-150">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="79657-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="79657-151">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="79657-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="79657-152">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="79657-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="79657-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79657-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="79657-154">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="79657-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="79657-155">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="79657-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="79657-156">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="79657-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79657-157">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="79657-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79657-158">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="79657-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="79657-159">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="79657-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="79657-160">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="79657-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="79657-161">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="79657-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="79657-162">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="79657-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="79657-163">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="79657-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="79657-164">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="79657-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="79657-165">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="79657-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="79657-166">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="79657-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="79657-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79657-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="79657-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79657-168">Remarks</span></span>

<span data-ttu-id="79657-169">La **clase \_ ClassicCOMClass de Win32** se deriva [**de \_ comClass de Win32**](win32-comclass.md).</span><span class="sxs-lookup"><span data-stu-id="79657-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79657-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79657-170">Requirements</span></span>



| <span data-ttu-id="79657-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="79657-171">Requirement</span></span> | <span data-ttu-id="79657-172">Value</span><span class="sxs-lookup"><span data-stu-id="79657-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79657-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79657-173">Minimum supported client</span></span><br/> | <span data-ttu-id="79657-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79657-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79657-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79657-175">Minimum supported server</span></span><br/> | <span data-ttu-id="79657-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79657-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79657-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79657-177">Namespace</span></span><br/>                | <span data-ttu-id="79657-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="79657-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79657-179">MOF</span><span class="sxs-lookup"><span data-stu-id="79657-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79657-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79657-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79657-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79657-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79657-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79657-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79657-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="79657-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79657-184">**Comclase Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="79657-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="79657-185">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79657-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

