---
description: Representa una asociación en la que los extremos de protocolo dependen de un servicio de reenvío para reenviar los datos.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: CIM_ForwardsAmong (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686513"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="36762-103">\_Clase ForwardsAmong de CIM</span><span class="sxs-lookup"><span data-stu-id="36762-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="36762-104">Representa una asociación en la que los extremos de protocolo dependen de un servicio de reenvío para reenviar los datos.</span><span class="sxs-lookup"><span data-stu-id="36762-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="36762-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36762-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="36762-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="36762-106">Members</span></span>

<span data-ttu-id="36762-107">La clase **CIM \_ ForwardsAmong** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36762-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="36762-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36762-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36762-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36762-109">Properties</span></span>

<span data-ttu-id="36762-110">La clase **CIM \_ ForwardsAmong** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="36762-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36762-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="36762-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36762-112">Tipo de datos **: \_ ProtocolEndpoint de CIM**</span><span class="sxs-lookup"><span data-stu-id="36762-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="36762-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36762-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36762-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="36762-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="36762-115">Los extremos del protocolo envían y reciben los datos reenviados.</span><span class="sxs-lookup"><span data-stu-id="36762-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="36762-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="36762-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36762-117">Tipo de datos: **CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="36762-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="36762-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36762-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36762-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="36762-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="36762-120">Servicio de reenvío que reenvía los datos.</span><span class="sxs-lookup"><span data-stu-id="36762-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36762-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36762-121">Requirements</span></span>



| <span data-ttu-id="36762-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36762-122">Requirement</span></span> | <span data-ttu-id="36762-123">Value</span><span class="sxs-lookup"><span data-stu-id="36762-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36762-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36762-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36762-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36762-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="36762-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36762-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36762-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="36762-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="36762-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36762-128">Namespace</span></span><br/>                | <span data-ttu-id="36762-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="36762-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36762-130">MOF</span><span class="sxs-lookup"><span data-stu-id="36762-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36762-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36762-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36762-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36762-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36762-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36762-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36762-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="36762-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36762-135">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="36762-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

