---
description: La \_ clase WMI abstracta ComClass de Win32 representa las propiedades de un componente del modelo de objetos componentes (com).
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Win32_COMClass (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000729"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="4890a-103">\_Clase de Comclase Win32</span><span class="sxs-lookup"><span data-stu-id="4890a-103">Win32\_COMClass class</span></span>

<span data-ttu-id="4890a-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ comClass de Win32** representa las propiedades de un componente del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="4890a-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="4890a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4890a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4890a-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4890a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4890a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4890a-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="4890a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4890a-108">Members</span></span>

<span data-ttu-id="4890a-109">La clase de **\_ comclase Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4890a-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="4890a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4890a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4890a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4890a-111">Properties</span></span>

<span data-ttu-id="4890a-112">La clase de **\_ comclase Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4890a-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4890a-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4890a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4890a-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4890a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4890a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4890a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4890a-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4890a-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4890a-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4890a-117">A short textual description of the object.</span></span>

<span data-ttu-id="4890a-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4890a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4890a-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4890a-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4890a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4890a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4890a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4890a-122">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="4890a-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4890a-123">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4890a-123">A textual description of the object.</span></span>

<span data-ttu-id="4890a-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4890a-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4890a-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4890a-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4890a-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4890a-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4890a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4890a-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="4890a-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4890a-129">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="4890a-129">Indicates when the object was installed.</span></span> <span data-ttu-id="4890a-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="4890a-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4890a-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4890a-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4890a-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4890a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4890a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4890a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4890a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4890a-135">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4890a-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4890a-136">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="4890a-136">Label by which the object is known.</span></span> <span data-ttu-id="4890a-137">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4890a-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4890a-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4890a-139">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4890a-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4890a-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4890a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4890a-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4890a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4890a-142">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4890a-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4890a-143">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4890a-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="4890a-144">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="4890a-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4890a-145">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="4890a-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4890a-146">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="4890a-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4890a-147">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="4890a-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4890a-148">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4890a-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4890a-149">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="4890a-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4890a-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4890a-151">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4890a-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4890a-152">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="4890a-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4890a-153">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="4890a-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4890a-154">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4890a-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4890a-155">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="4890a-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4890a-156">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="4890a-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4890a-157">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="4890a-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4890a-158">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="4890a-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4890a-159">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="4890a-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4890a-160">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="4890a-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4890a-161">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4890a-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4890a-162">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="4890a-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4890a-163">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="4890a-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4890a-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4890a-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4890a-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4890a-165">Remarks</span></span>

<span data-ttu-id="4890a-166">La clase de **\_ comclase Win32** se deriva [**de \_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4890a-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4890a-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4890a-167">Requirements</span></span>



| <span data-ttu-id="4890a-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="4890a-168">Requirement</span></span> | <span data-ttu-id="4890a-169">Value</span><span class="sxs-lookup"><span data-stu-id="4890a-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4890a-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4890a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4890a-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4890a-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4890a-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4890a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4890a-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4890a-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4890a-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4890a-174">Namespace</span></span><br/>                | <span data-ttu-id="4890a-175">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4890a-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4890a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4890a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4890a-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4890a-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4890a-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4890a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4890a-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4890a-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4890a-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="4890a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4890a-181">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4890a-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="4890a-182">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4890a-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

