---
description: La \_ clase WMI abstracta Comapplication de Win32 representa una aplicación com (modelo de objetos componentes). En este contexto, una aplicación COM es una agrupación lógica de clases COM.
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Win32_COMApplication (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080254"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="51c16-104">\_Clase Comapplication de Win32</span><span class="sxs-lookup"><span data-stu-id="51c16-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="51c16-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ comapplication de Win32** representa una aplicación com (modelo de objetos componentes).</span><span class="sxs-lookup"><span data-stu-id="51c16-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="51c16-106">En este contexto, una aplicación COM es una agrupación lógica de clases COM.</span><span class="sxs-lookup"><span data-stu-id="51c16-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="51c16-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="51c16-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="51c16-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="51c16-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c16-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51c16-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="51c16-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="51c16-110">Members</span></span>

<span data-ttu-id="51c16-111">La **clase \_ comapplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="51c16-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="51c16-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51c16-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51c16-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51c16-113">Properties</span></span>

<span data-ttu-id="51c16-114">La **clase \_ Comapplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="51c16-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51c16-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="51c16-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c16-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51c16-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c16-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="51c16-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c16-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="51c16-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="51c16-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="51c16-119">A short textual description of the object.</span></span>

<span data-ttu-id="51c16-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c16-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51c16-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c16-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51c16-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c16-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="51c16-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c16-124">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="51c16-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="51c16-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="51c16-125">A textual description of the object.</span></span>

<span data-ttu-id="51c16-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c16-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="51c16-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c16-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51c16-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51c16-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="51c16-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c16-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="51c16-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="51c16-131">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="51c16-131">Indicates when the object was installed.</span></span> <span data-ttu-id="51c16-132">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="51c16-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="51c16-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c16-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="51c16-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c16-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51c16-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c16-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="51c16-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c16-137">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="51c16-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="51c16-138">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="51c16-138">Label by which the object is known.</span></span> <span data-ttu-id="51c16-139">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="51c16-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="51c16-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c16-141">**Estado**</span><span class="sxs-lookup"><span data-stu-id="51c16-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c16-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51c16-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c16-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="51c16-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c16-144">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="51c16-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="51c16-145">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="51c16-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="51c16-146">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="51c16-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="51c16-147">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="51c16-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="51c16-148">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="51c16-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="51c16-149">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="51c16-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="51c16-150">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="51c16-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="51c16-151">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="51c16-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="51c16-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="51c16-153">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="51c16-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="51c16-154">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="51c16-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="51c16-155">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="51c16-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="51c16-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="51c16-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="51c16-157">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="51c16-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="51c16-158">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="51c16-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="51c16-159">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="51c16-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="51c16-160">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="51c16-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="51c16-161">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="51c16-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="51c16-162">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="51c16-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="51c16-163">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="51c16-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="51c16-164">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="51c16-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="51c16-165">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="51c16-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="51c16-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="51c16-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="51c16-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51c16-167">Remarks</span></span>

<span data-ttu-id="51c16-168">La clase de **\_ comaplicación Win32** se deriva [**de \_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="51c16-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51c16-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51c16-169">Requirements</span></span>



| <span data-ttu-id="51c16-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c16-170">Requirement</span></span> | <span data-ttu-id="51c16-171">Value</span><span class="sxs-lookup"><span data-stu-id="51c16-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51c16-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c16-172">Minimum supported client</span></span><br/> | <span data-ttu-id="51c16-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51c16-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51c16-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c16-174">Minimum supported server</span></span><br/> | <span data-ttu-id="51c16-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51c16-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51c16-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51c16-176">Namespace</span></span><br/>                | <span data-ttu-id="51c16-177">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="51c16-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51c16-178">MOF</span><span class="sxs-lookup"><span data-stu-id="51c16-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51c16-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51c16-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51c16-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51c16-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51c16-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51c16-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c16-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="51c16-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c16-183">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="51c16-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="51c16-184">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51c16-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

