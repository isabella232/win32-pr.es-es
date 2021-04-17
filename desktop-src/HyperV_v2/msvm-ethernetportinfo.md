---
description: Una asociación entre una instancia de la \_ clase MSVM EthernetSwitchPort y una instancia de la \_ clase MSVM EthernetPortData que representa los datos recopilados sobre el puerto mediante una extensión de conmutador.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687645"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="f6d4e-103">MSVM \_ EthernetPortInfo (clase)</span><span class="sxs-lookup"><span data-stu-id="f6d4e-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="f6d4e-104">Una asociación entre una instancia de la clase [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) y una instancia de la clase [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) que representa los datos recopilados sobre el puerto mediante una extensión de conmutador.</span><span class="sxs-lookup"><span data-stu-id="f6d4e-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="f6d4e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6d4e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d4e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6d4e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f6d4e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6d4e-107">Members</span></span>

<span data-ttu-id="f6d4e-108">La clase **MSVM \_ EthernetPortInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6d4e-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="f6d4e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6d4e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6d4e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6d4e-110">Properties</span></span>

<span data-ttu-id="f6d4e-111">La clase **MSVM \_ EthernetPortInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6d4e-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6d4e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f6d4e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6d4e-113">Tipo de datos: **MSVM \_ EthernetSwitchPort**</span><span class="sxs-lookup"><span data-stu-id="f6d4e-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="f6d4e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6d4e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6d4e-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="f6d4e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f6d4e-116">Instancia de la clase [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa el puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="f6d4e-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="f6d4e-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f6d4e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6d4e-118">Tipo de datos: **MSVM \_ EthernetPortData**</span><span class="sxs-lookup"><span data-stu-id="f6d4e-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="f6d4e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6d4e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6d4e-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="f6d4e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f6d4e-121">Instancia de la clase [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) que representa los datos del puerto.</span><span class="sxs-lookup"><span data-stu-id="f6d4e-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6d4e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6d4e-122">Requirements</span></span>



| <span data-ttu-id="f6d4e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d4e-123">Requirement</span></span> | <span data-ttu-id="f6d4e-124">Value</span><span class="sxs-lookup"><span data-stu-id="f6d4e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d4e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6d4e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d4e-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6d4e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6d4e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6d4e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d4e-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6d4e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6d4e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6d4e-129">Namespace</span></span><br/>                | <span data-ttu-id="f6d4e-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6d4e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6d4e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f6d4e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6d4e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6d4e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6d4e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6d4e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d4e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6d4e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

