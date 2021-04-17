---
description: La \_ clase WMI DCOMApplication de Win32 representa las propiedades de una aplicación DCOM.
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Win32_DCOMApplication (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659748"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="64e3d-103">\_Clase Win32 DCOMApplication</span><span class="sxs-lookup"><span data-stu-id="64e3d-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="64e3d-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplication de Win32** representa las propiedades de una aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="64e3d-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="64e3d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="64e3d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64e3d-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="64e3d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e3d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64e3d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="64e3d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="64e3d-108">Members</span></span>

<span data-ttu-id="64e3d-109">La **clase \_ DCOMApplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="64e3d-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="64e3d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64e3d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64e3d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64e3d-111">Properties</span></span>

<span data-ttu-id="64e3d-112">La **clase \_ DCOMApplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="64e3d-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64e3d-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="64e3d-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64e3d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-116">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="64e3d-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-117">Identificador único global (GUID) para la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="64e3d-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="64e3d-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="64e3d-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64e3d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="64e3d-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3d-122">A short textual description of the object.</span></span>

<span data-ttu-id="64e3d-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64e3d-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64e3d-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64e3d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-127">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="64e3d-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-128">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3d-128">A textual description of the object.</span></span>

<span data-ttu-id="64e3d-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64e3d-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="64e3d-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="64e3d-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-133">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="64e3d-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-134">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3d-134">Indicates when the object was installed.</span></span> <span data-ttu-id="64e3d-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="64e3d-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="64e3d-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64e3d-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="64e3d-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64e3d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-140">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="64e3d-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-141">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3d-141">Label by which the object is known.</span></span> <span data-ttu-id="64e3d-142">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="64e3d-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="64e3d-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64e3d-144">**Estado**</span><span class="sxs-lookup"><span data-stu-id="64e3d-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64e3d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64e3d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64e3d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64e3d-147">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="64e3d-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="64e3d-148">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="64e3d-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="64e3d-149">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="64e3d-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="64e3d-150">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="64e3d-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="64e3d-151">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="64e3d-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="64e3d-152">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="64e3d-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="64e3d-153">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="64e3d-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="64e3d-154">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="64e3d-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="64e3d-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="64e3d-156">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="64e3d-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="64e3d-157">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="64e3d-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="64e3d-158">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="64e3d-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="64e3d-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="64e3d-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64e3d-160">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="64e3d-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="64e3d-161">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="64e3d-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="64e3d-162">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="64e3d-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="64e3d-163">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="64e3d-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="64e3d-164">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="64e3d-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="64e3d-165">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="64e3d-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="64e3d-166">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="64e3d-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="64e3d-167">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="64e3d-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="64e3d-168">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="64e3d-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="64e3d-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="64e3d-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="64e3d-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64e3d-170">Remarks</span></span>

<span data-ttu-id="64e3d-171">La **clase \_ DCOMApplication de Win32** se deriva de la [**\_ comaplicación Win32**](win32-comapplication.md).</span><span class="sxs-lookup"><span data-stu-id="64e3d-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64e3d-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64e3d-172">Requirements</span></span>



| <span data-ttu-id="64e3d-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="64e3d-173">Requirement</span></span> | <span data-ttu-id="64e3d-174">Value</span><span class="sxs-lookup"><span data-stu-id="64e3d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64e3d-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64e3d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="64e3d-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64e3d-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64e3d-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64e3d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="64e3d-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64e3d-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64e3d-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64e3d-179">Namespace</span></span><br/>                | <span data-ttu-id="64e3d-180">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="64e3d-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64e3d-181">MOF</span><span class="sxs-lookup"><span data-stu-id="64e3d-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64e3d-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64e3d-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64e3d-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64e3d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64e3d-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e3d-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e3d-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="64e3d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e3d-186">**Comaplicación Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="64e3d-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="64e3d-187">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64e3d-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

