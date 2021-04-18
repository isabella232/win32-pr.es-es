---
description: Esta asociación indica que una subclase del dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687267"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="00b1c-103">MSVM \_ ProtocolControllerForUnit (clase)</span><span class="sxs-lookup"><span data-stu-id="00b1c-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="00b1c-104">Esta asociación indica que una subclase del dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.</span><span class="sxs-lookup"><span data-stu-id="00b1c-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="00b1c-105">En muchas situaciones (por ejemplo, el enmascaramiento de LUN de almacenamiento), es posible que haya muchas de estas asociaciones utilizadas para relacionar los distintos objetos.</span><span class="sxs-lookup"><span data-stu-id="00b1c-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="00b1c-106">Por lo tanto, se han definido subclases para optimizar la enumeración de las asociaciones.</span><span class="sxs-lookup"><span data-stu-id="00b1c-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="00b1c-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="00b1c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b1c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00b1c-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="00b1c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="00b1c-109">Members</span></span>

<span data-ttu-id="00b1c-110">La clase **MSVM \_ ProtocolControllerForUnit** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="00b1c-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="00b1c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00b1c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00b1c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00b1c-112">Properties</span></span>

<span data-ttu-id="00b1c-113">La clase **MSVM \_ ProtocolControllerForUnit** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="00b1c-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00b1c-114">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="00b1c-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-115">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00b1c-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-117">La prioridad dada para acceder al dispositivo a través de este controlador.</span><span class="sxs-lookup"><span data-stu-id="00b1c-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="00b1c-118">La ruta de acceso de prioridad más alta tendrá el valor más bajo para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="00b1c-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="00b1c-119">Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="00b1c-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="00b1c-120">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="00b1c-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-121">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00b1c-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-123">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo (2) o no (3).</span><span class="sxs-lookup"><span data-stu-id="00b1c-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="00b1c-124">Además, se puede definir el valor 0 (desconocido).</span><span class="sxs-lookup"><span data-stu-id="00b1c-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="00b1c-125">Esta información es necesaria cuando un dispositivo lógico puede ser comando por varios controladores de protocolo o tener acceso a ellos a través de ellos.</span><span class="sxs-lookup"><span data-stu-id="00b1c-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="00b1c-126">Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="00b1c-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="00b1c-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="00b1c-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Activo** (2)</span><span class="sxs-lookup"><span data-stu-id="00b1c-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactivo** (3)</span><span class="sxs-lookup"><span data-stu-id="00b1c-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00b1c-130">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="00b1c-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-131">Tipo de datos: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="00b1c-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-133">El controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="00b1c-133">The protocol controller.</span></span> <span data-ttu-id="00b1c-134">Esta clase se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="00b1c-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="00b1c-135">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="00b1c-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-136">Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="00b1c-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-138">El dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="00b1c-138">The controlled device.</span></span> <span data-ttu-id="00b1c-139">Esta clase se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="00b1c-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="00b1c-140">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="00b1c-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00b1c-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-143">Los derechos de acceso concedidos al dispositivo a través de este controlador.</span><span class="sxs-lookup"><span data-stu-id="00b1c-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="00b1c-144">Esta clase se hereda de **\_ ProtocolControllerForUnit CIM**.</span><span class="sxs-lookup"><span data-stu-id="00b1c-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="00b1c-145">Value</span><span class="sxs-lookup"><span data-stu-id="00b1c-145">Value</span></span>                                                                               | <span data-ttu-id="00b1c-146">Significado</span><span class="sxs-lookup"><span data-stu-id="00b1c-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="00b1c-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="00b1c-148">Unknown</span><span class="sxs-lookup"><span data-stu-id="00b1c-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="00b1c-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="00b1c-150">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="00b1c-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="00b1c-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="00b1c-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="00b1c-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="00b1c-154">Sin acceso.</span><span class="sxs-lookup"><span data-stu-id="00b1c-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="00b1c-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="00b1c-156">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="00b1c-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="00b1c-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="00b1c-158">Proveedor reservado</span><span class="sxs-lookup"><span data-stu-id="00b1c-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="00b1c-159">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="00b1c-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b1c-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00b1c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00b1c-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00b1c-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b1c-162">La dirección del dispositivo asociado en el contexto del controlador antecedente.</span><span class="sxs-lookup"><span data-stu-id="00b1c-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="00b1c-163">Esta clase se hereda de **\_ ProtocolControllerForDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="00b1c-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00b1c-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00b1c-164">Remarks</span></span>

<span data-ttu-id="00b1c-165">El acceso a la clase **MSVM \_ ProtocolControllerForUnit** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="00b1c-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="00b1c-166">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="00b1c-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="00b1c-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b1c-167">Requirements</span></span>



| <span data-ttu-id="00b1c-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b1c-168">Requirement</span></span> | <span data-ttu-id="00b1c-169">Value</span><span class="sxs-lookup"><span data-stu-id="00b1c-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00b1c-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00b1c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="00b1c-171">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="00b1c-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="00b1c-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00b1c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="00b1c-173">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="00b1c-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00b1c-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00b1c-174">Namespace</span></span><br/>                | <span data-ttu-id="00b1c-175">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="00b1c-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="00b1c-176">MOF</span><span class="sxs-lookup"><span data-stu-id="00b1c-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00b1c-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00b1c-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00b1c-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00b1c-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00b1c-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00b1c-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="00b1c-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b1c-181">**\_PROTOCOLCONTROLLERFORUNIT CIM**</span><span class="sxs-lookup"><span data-stu-id="00b1c-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="00b1c-182">[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00b1c-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="00b1c-183">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="00b1c-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

