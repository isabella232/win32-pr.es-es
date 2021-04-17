---
description: Representa una asociación en la que una entrada de una base de datos de reenvío se aplica a un puerto de conmutador.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: CIM_SwitchPortDynamicForwarding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666913"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="15b7a-103">\_Clase SwitchPortDynamicForwarding de CIM</span><span class="sxs-lookup"><span data-stu-id="15b7a-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="15b7a-104">Representa una asociación en la que una entrada de una base de datos de reenvío se aplica a un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="15b7a-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15b7a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="15b7a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="15b7a-106">Members</span></span>

<span data-ttu-id="15b7a-107">La clase **CIM \_ SwitchPortDynamicForwarding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15b7a-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="15b7a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15b7a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15b7a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15b7a-109">Properties</span></span>

<span data-ttu-id="15b7a-110">La clase **CIM \_ SwitchPortDynamicForwarding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15b7a-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15b7a-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="15b7a-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b7a-112">Tipo de datos **: \_ SwitchPort de CIM**</span><span class="sxs-lookup"><span data-stu-id="15b7a-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="15b7a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15b7a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15b7a-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="15b7a-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="15b7a-115">Una referencia de [**\_ SwitchPort de CIM**](cim-switchport.md) al puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="15b7a-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="15b7a-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="15b7a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b7a-117">Tipo de datos: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="15b7a-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="15b7a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15b7a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15b7a-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="15b7a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="15b7a-120">Referencia [**de \_ DynamicForwardingEntry de CIM**](cim-dynamicforwardingentry.md) a la entrada de la base de datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="15b7a-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15b7a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15b7a-121">Requirements</span></span>



| <span data-ttu-id="15b7a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b7a-122">Requirement</span></span> | <span data-ttu-id="15b7a-123">Value</span><span class="sxs-lookup"><span data-stu-id="15b7a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b7a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15b7a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15b7a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15b7a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15b7a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15b7a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15b7a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15b7a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15b7a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15b7a-128">Namespace</span></span><br/>                | <span data-ttu-id="15b7a-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="15b7a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15b7a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="15b7a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15b7a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15b7a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15b7a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15b7a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15b7a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15b7a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15b7a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="15b7a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b7a-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="15b7a-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

