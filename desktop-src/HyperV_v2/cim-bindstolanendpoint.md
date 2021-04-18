---
description: Representa una asociación en la que un \_ objeto ProtocolEndpoint CIM punto o CIM \_ depende de un \_ objeto LANEndpoint CIM subyacente en el mismo sistema.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668136"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="f08de-103">\_Clase BindsToLANEndpoint de CIM</span><span class="sxs-lookup"><span data-stu-id="f08de-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="f08de-104">Representa una asociación en la que un objeto [**\_ ProtocolEndpoint**](cim-protocolendpoint.md) CIM [**\_ punto**](cim-serviceaccesspoint.md) o CIM depende de un objeto [**\_ LANEndpoint CIM**](cim-lanendpoint.md) subyacente en el mismo sistema.</span><span class="sxs-lookup"><span data-stu-id="f08de-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f08de-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="f08de-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f08de-106">Members</span></span>

<span data-ttu-id="f08de-107">La clase **CIM \_ BindsToLANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f08de-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="f08de-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f08de-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f08de-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f08de-109">Properties</span></span>

<span data-ttu-id="f08de-110">La clase **CIM \_ BindsToLANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f08de-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f08de-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f08de-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f08de-112">Tipo de datos: **CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f08de-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="f08de-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f08de-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f08de-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f08de-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f08de-115">Objeto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) subyacente.</span><span class="sxs-lookup"><span data-stu-id="f08de-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f08de-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f08de-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f08de-117">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="f08de-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="f08de-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f08de-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f08de-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="f08de-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f08de-120">Objeto de CIM [**\_ punto**](cim-serviceaccesspoint.md) o [**CIM \_**](cim-protocolendpoint.md) que depende del [**\_ LANEndpoint CIM**](cim-lanendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="f08de-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f08de-121">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="f08de-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f08de-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f08de-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f08de-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f08de-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f08de-124">Método de tramas para el punto de acceso del servicio de nivel superior o el extremo del protocolo.</span><span class="sxs-lookup"><span data-stu-id="f08de-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="f08de-125">Solo se sabe usar 802.3 sin formato con el protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="f08de-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f08de-126">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f08de-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="f08de-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="f08de-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="f08de-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="f08de-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="f08de-129">**Ajustar** (3)</span><span class="sxs-lookup"><span data-stu-id="f08de-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="f08de-130">**802.3 sin formato** (4)</span><span class="sxs-lookup"><span data-stu-id="f08de-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="f08de-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f08de-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f08de-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f08de-132">Requirements</span></span>



| <span data-ttu-id="f08de-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f08de-133">Requirement</span></span> | <span data-ttu-id="f08de-134">Value</span><span class="sxs-lookup"><span data-stu-id="f08de-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08de-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f08de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f08de-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f08de-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f08de-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f08de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f08de-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f08de-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f08de-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f08de-139">Namespace</span></span><br/>                | <span data-ttu-id="f08de-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f08de-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f08de-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f08de-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f08de-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f08de-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f08de-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f08de-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f08de-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f08de-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f08de-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f08de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08de-146">**\_BINDSTO CIM**</span><span class="sxs-lookup"><span data-stu-id="f08de-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

