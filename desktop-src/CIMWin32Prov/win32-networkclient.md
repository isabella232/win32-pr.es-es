---
description: La \_ clase WMI NetworkClient de Win32 representa un cliente de red en un sistema Windows. Cualquier sistema informático de la red con una relación de cliente con el sistema es un descendiente (o miembro) de esta clase.
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Win32_NetworkClient (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000758"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="59027-104">\_Clase Win32 NetworkClient</span><span class="sxs-lookup"><span data-stu-id="59027-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="59027-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkClient de Win32** representa un cliente de red en un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="59027-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="59027-106">Cualquier sistema informático de la red con una relación de cliente con el sistema es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="59027-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="59027-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="59027-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="59027-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="59027-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59027-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59027-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="59027-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="59027-110">Members</span></span>

<span data-ttu-id="59027-111">La **clase \_ NetworkClient de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="59027-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="59027-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59027-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59027-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59027-113">Properties</span></span>

<span data-ttu-id="59027-114">La **clase \_ NetworkClient de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="59027-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59027-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="59027-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59027-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59027-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-118">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="59027-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="59027-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="59027-119">A short textual description of the object.</span></span>

<span data-ttu-id="59027-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59027-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59027-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59027-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59027-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59027-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-124">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="59027-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="59027-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="59027-125">A textual description of the object.</span></span>

<span data-ttu-id="59027-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59027-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59027-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="59027-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="59027-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59027-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-130">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="59027-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="59027-131">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="59027-131">Indicates when the object was installed.</span></span> <span data-ttu-id="59027-132">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="59027-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="59027-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59027-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59027-134">**Le**</span><span class="sxs-lookup"><span data-stu-id="59027-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59027-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59027-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| Mfg")</span><span class="sxs-lookup"><span data-stu-id="59027-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="59027-138">Nombre del fabricante del cliente de red que se ejecuta en el equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="59027-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="59027-139">Ejemplo: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="59027-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="59027-140">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="59027-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59027-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59027-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-143">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| Name")</span><span class="sxs-lookup"><span data-stu-id="59027-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="59027-144">Nombre de red del cliente de red que se ejecuta en el equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="59027-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="59027-145">Ejemplo: "red de Microsoft Windows"</span><span class="sxs-lookup"><span data-stu-id="59027-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="59027-146">**Estado**</span><span class="sxs-lookup"><span data-stu-id="59027-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59027-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="59027-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59027-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="59027-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59027-149">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="59027-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="59027-150">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="59027-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="59027-151">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="59027-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="59027-152">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="59027-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="59027-153">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="59027-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="59027-154">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="59027-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="59027-155">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="59027-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="59027-156">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="59027-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="59027-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59027-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="59027-158">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="59027-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="59027-159">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="59027-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="59027-160">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="59027-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="59027-161">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="59027-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="59027-162">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="59027-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="59027-163">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="59027-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="59027-164">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="59027-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="59027-165">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="59027-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="59027-166">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="59027-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="59027-167">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="59027-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="59027-168">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="59027-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="59027-169">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="59027-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="59027-170">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="59027-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="59027-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="59027-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="59027-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59027-172">Remarks</span></span>

<span data-ttu-id="59027-173">La **clase \_ NetworkClient de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59027-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59027-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59027-174">Requirements</span></span>



| <span data-ttu-id="59027-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="59027-175">Requirement</span></span> | <span data-ttu-id="59027-176">Value</span><span class="sxs-lookup"><span data-stu-id="59027-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59027-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59027-177">Minimum supported client</span></span><br/> | <span data-ttu-id="59027-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59027-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59027-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59027-179">Minimum supported server</span></span><br/> | <span data-ttu-id="59027-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59027-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59027-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59027-181">Namespace</span></span><br/>                | <span data-ttu-id="59027-182">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="59027-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59027-183">MOF</span><span class="sxs-lookup"><span data-stu-id="59027-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59027-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59027-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59027-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59027-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59027-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59027-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59027-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="59027-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59027-188">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="59027-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="59027-189">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="59027-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
