---
description: Conecta un puerto del conmutador a una entrada de reenvío dinámica (dirección MAC aprendida).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687328"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="80d72-103">MSVM \_ SwitchPortDynamicForwarding (clase)</span><span class="sxs-lookup"><span data-stu-id="80d72-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="80d72-104">Conecta un puerto del conmutador a una entrada de reenvío dinámica (dirección MAC aprendida).</span><span class="sxs-lookup"><span data-stu-id="80d72-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="80d72-105">Esto resulta útil para buscar todas las direcciones MAC aprendidas para un puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="80d72-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="80d72-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="80d72-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d72-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80d72-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="80d72-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="80d72-108">Members</span></span>

<span data-ttu-id="80d72-109">La clase **MSVM \_ SwitchPortDynamicForwarding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80d72-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="80d72-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80d72-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80d72-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80d72-111">Properties</span></span>

<span data-ttu-id="80d72-112">La clase **MSVM \_ SwitchPortDynamicForwarding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="80d72-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80d72-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="80d72-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d72-114">Tipo de datos: **[ **MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="80d72-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="80d72-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80d72-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80d72-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="80d72-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="80d72-117">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa el puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="80d72-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="80d72-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="80d72-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d72-119">Tipo de datos: **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="80d72-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="80d72-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80d72-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80d72-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="80d72-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="80d72-122">Referencia a una instancia de la clase [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa la entrada de reenvío dinámico de la base de datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="80d72-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80d72-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80d72-123">Remarks</span></span>

<span data-ttu-id="80d72-124">El acceso a la clase **MSVM \_ SwitchPortDynamicForwarding** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="80d72-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="80d72-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="80d72-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="80d72-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="80d72-126">Examples</span></span>

<span data-ttu-id="80d72-127">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="80d72-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80d72-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80d72-128">Requirements</span></span>



| <span data-ttu-id="80d72-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="80d72-129">Requirement</span></span> | <span data-ttu-id="80d72-130">Value</span><span class="sxs-lookup"><span data-stu-id="80d72-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d72-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80d72-131">Minimum supported client</span></span><br/> | <span data-ttu-id="80d72-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="80d72-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80d72-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80d72-133">Minimum supported server</span></span><br/> | <span data-ttu-id="80d72-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="80d72-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80d72-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80d72-135">Namespace</span></span><br/>                | <span data-ttu-id="80d72-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="80d72-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80d72-137">MOF</span><span class="sxs-lookup"><span data-stu-id="80d72-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80d72-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80d72-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80d72-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80d72-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80d72-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80d72-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80d72-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="80d72-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d72-142">**\_SWITCHPORTDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="80d72-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="80d72-143">[**\_SWITCHPORTDYNAMICFORWARDING CIM**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80d72-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

