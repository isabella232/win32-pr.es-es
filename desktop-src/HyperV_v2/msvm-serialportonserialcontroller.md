---
description: Asocia un puerto serie a un controlador serie.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908191"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="b89e5-103">MSVM \_ SerialPortOnSerialController (clase)</span><span class="sxs-lookup"><span data-stu-id="b89e5-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="b89e5-104">Asocia un puerto serie a un controlador serie.</span><span class="sxs-lookup"><span data-stu-id="b89e5-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="b89e5-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b89e5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89e5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b89e5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b89e5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b89e5-107">Members</span></span>

<span data-ttu-id="b89e5-108">La clase **MSVM \_ SerialPortOnSerialController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b89e5-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="b89e5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b89e5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b89e5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b89e5-110">Properties</span></span>

<span data-ttu-id="b89e5-111">La clase **MSVM \_ SerialPortOnSerialController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b89e5-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b89e5-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b89e5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89e5-113">Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="b89e5-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="b89e5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b89e5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89e5-115">Controlador serie al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="b89e5-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="b89e5-116">Esta propiedad se hereda de [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="b89e5-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="b89e5-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b89e5-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89e5-118">Tipo de datos: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b89e5-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b89e5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b89e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89e5-120">Puerto del controlador serie.</span><span class="sxs-lookup"><span data-stu-id="b89e5-120">The port of the serial controller.</span></span> <span data-ttu-id="b89e5-121">Esta propiedad se hereda de [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="b89e5-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b89e5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b89e5-122">Remarks</span></span>

<span data-ttu-id="b89e5-123">El acceso a la clase **MSVM \_ SerialPortOnSerialController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b89e5-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b89e5-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b89e5-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b89e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89e5-125">Requirements</span></span>



| <span data-ttu-id="b89e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b89e5-126">Requirement</span></span> | <span data-ttu-id="b89e5-127">Value</span><span class="sxs-lookup"><span data-stu-id="b89e5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89e5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b89e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b89e5-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b89e5-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b89e5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b89e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b89e5-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b89e5-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b89e5-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b89e5-132">Namespace</span></span><br/>                | <span data-ttu-id="b89e5-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b89e5-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b89e5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b89e5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b89e5-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b89e5-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b89e5-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b89e5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b89e5-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b89e5-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b89e5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b89e5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89e5-139">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b89e5-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="b89e5-140">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b89e5-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="b89e5-141">Clases de dispositivos serie</span><span class="sxs-lookup"><span data-stu-id="b89e5-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

