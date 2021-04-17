---
description: Representa una asociación en la que un \_ objeto punto de CIM solicita servicios de protocolo de un \_ objeto PROTOCOLENDPOINT de CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: CIM_BindsTo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667689"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="7df54-103">\_Clase BindsTo de CIM</span><span class="sxs-lookup"><span data-stu-id="7df54-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="7df54-104">Representa una asociación en la que un objeto [**\_ punto de CIM**](cim-serviceaccesspoint.md) solicita servicios de protocolo de un objeto [**\_ ProtocolEndpoint de CIM**](cim-protocolendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="7df54-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7df54-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7df54-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7df54-106">Members</span></span>

<span data-ttu-id="7df54-107">La clase **CIM \_ BindsTo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7df54-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="7df54-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7df54-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7df54-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7df54-109">Properties</span></span>

<span data-ttu-id="7df54-110">La clase **CIM \_ BindsTo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7df54-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7df54-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7df54-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7df54-112">Tipo de datos **: \_ ProtocolEndpoint de CIM**</span><span class="sxs-lookup"><span data-stu-id="7df54-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="7df54-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7df54-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7df54-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7df54-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7df54-115">Extremo de nivel inferior al que tiene acceso el punto de acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="7df54-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="7df54-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="7df54-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7df54-117">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="7df54-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="7df54-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7df54-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7df54-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="7df54-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7df54-120">Punto de acceso o punto de conexión de protocolo que depende del punto de conexión de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="7df54-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7df54-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df54-121">Requirements</span></span>



| <span data-ttu-id="7df54-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df54-122">Requirement</span></span> | <span data-ttu-id="7df54-123">Value</span><span class="sxs-lookup"><span data-stu-id="7df54-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df54-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df54-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7df54-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7df54-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7df54-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df54-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7df54-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7df54-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7df54-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7df54-128">Namespace</span></span><br/>                | <span data-ttu-id="7df54-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7df54-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7df54-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7df54-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7df54-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7df54-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7df54-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7df54-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df54-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7df54-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7df54-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df54-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df54-135">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="7df54-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

