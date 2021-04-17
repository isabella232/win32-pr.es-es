---
description: Asocia un servicio de puente transparente a una entrada de su base de datos de reenvío.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: CIM_TransparentBridgingDynamicForwarding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666906"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="1bf1a-103">\_Clase TransparentBridgingDynamicForwarding de CIM</span><span class="sxs-lookup"><span data-stu-id="1bf1a-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="1bf1a-104">Asocia un servicio de puente transparente a una entrada de su base de datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="1bf1a-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1bf1a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1bf1a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1bf1a-106">Members</span></span>

<span data-ttu-id="1bf1a-107">La clase **CIM \_ TransparentBridgingDynamicForwarding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1bf1a-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf1a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bf1a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf1a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bf1a-109">Properties</span></span>

<span data-ttu-id="1bf1a-110">La clase **CIM \_ TransparentBridgingDynamicForwarding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1bf1a-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bf1a-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1bf1a-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf1a-112">Tipo de datos: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="1bf1a-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="1bf1a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bf1a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf1a-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1bf1a-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1bf1a-115">Una [**referencia \_ TransparentBridgingService de CIM**](cim-transparentbridgingservice.md) al servicio de puente transparente.</span><span class="sxs-lookup"><span data-stu-id="1bf1a-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="1bf1a-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1bf1a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf1a-117">Tipo de datos: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="1bf1a-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="1bf1a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bf1a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf1a-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1bf1a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1bf1a-120">Referencia [**de \_ DynamicForwardingEntry de CIM**](cim-dynamicforwardingentry.md) a la entrada de la base de datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="1bf1a-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bf1a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf1a-121">Requirements</span></span>



| <span data-ttu-id="1bf1a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf1a-122">Requirement</span></span> | <span data-ttu-id="1bf1a-123">Value</span><span class="sxs-lookup"><span data-stu-id="1bf1a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf1a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bf1a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf1a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1bf1a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1bf1a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bf1a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf1a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1bf1a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1bf1a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1bf1a-128">Namespace</span></span><br/>                | <span data-ttu-id="1bf1a-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1bf1a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1bf1a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1bf1a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bf1a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bf1a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bf1a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1bf1a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf1a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bf1a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1bf1a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bf1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf1a-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1bf1a-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

