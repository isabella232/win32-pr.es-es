---
description: Representa un servicio de conmutador, que cambia fotogramas entre puertos de conmutador.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: CIM_SwitchesAmong (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154536"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="3ad0a-103">\_Clase SwitchesAmong de CIM</span><span class="sxs-lookup"><span data-stu-id="3ad0a-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="3ad0a-104">Representa un servicio de conmutador, que cambia fotogramas entre puertos de conmutador.</span><span class="sxs-lookup"><span data-stu-id="3ad0a-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ad0a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3ad0a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ad0a-106">Members</span></span>

<span data-ttu-id="3ad0a-107">La clase **CIM \_ SwitchesAmong** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ad0a-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="3ad0a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ad0a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ad0a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ad0a-109">Properties</span></span>

<span data-ttu-id="3ad0a-110">La clase **CIM \_ SwitchesAmong** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ad0a-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ad0a-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3ad0a-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad0a-112">Tipo de datos **: \_ SwitchPort de CIM**</span><span class="sxs-lookup"><span data-stu-id="3ad0a-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="3ad0a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ad0a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ad0a-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3ad0a-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3ad0a-115">Una referencia de [**\_ SwitchPort de CIM**](cim-switchport.md) al puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="3ad0a-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="3ad0a-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3ad0a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad0a-117">Tipo de datos: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="3ad0a-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="3ad0a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ad0a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ad0a-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="3ad0a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3ad0a-120">Una [**referencia \_ SwitchService de CIM**](cim-switchservice.md) al servicio de conmutación.</span><span class="sxs-lookup"><span data-stu-id="3ad0a-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ad0a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad0a-121">Requirements</span></span>



| <span data-ttu-id="3ad0a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad0a-122">Requirement</span></span> | <span data-ttu-id="3ad0a-123">Value</span><span class="sxs-lookup"><span data-stu-id="3ad0a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad0a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad0a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad0a-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3ad0a-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3ad0a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad0a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad0a-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ad0a-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3ad0a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ad0a-128">Namespace</span></span><br/>                | <span data-ttu-id="3ad0a-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3ad0a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ad0a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3ad0a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ad0a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ad0a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ad0a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ad0a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad0a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ad0a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ad0a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ad0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad0a-135">**\_FORWARDSAMONG CIM**</span><span class="sxs-lookup"><span data-stu-id="3ad0a-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

