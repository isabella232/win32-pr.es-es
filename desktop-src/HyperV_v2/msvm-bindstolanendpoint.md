---
description: Esta asociación establece un punto de acceso al servicio (SAP) como solicitante de servicios de protocolo desde un punto de conexión de protocolo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002788"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="1092f-103">MSVM \_ BindsToLANEndpoint (clase)</span><span class="sxs-lookup"><span data-stu-id="1092f-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="1092f-104">Esta asociación establece un punto de acceso al servicio (SAP) como solicitante de servicios de protocolo desde un punto de conexión de protocolo.</span><span class="sxs-lookup"><span data-stu-id="1092f-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="1092f-105">Normalmente, esta asociación se ejecuta entre SAP y los puntos de conexión en un único sistema.</span><span class="sxs-lookup"><span data-stu-id="1092f-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="1092f-106">Dado que un punto de conexión de protocolo es un tipo de SAP, este enlace se puede usar para establecer una capa de dos protocolos, con la capa superior representada por el **dependiente** y la capa inferior representada por el **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="1092f-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="1092f-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1092f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1092f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1092f-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="1092f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1092f-109">Members</span></span>

<span data-ttu-id="1092f-110">La clase **MSVM \_ BindsToLANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1092f-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="1092f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1092f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1092f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1092f-112">Properties</span></span>

<span data-ttu-id="1092f-113">La clase **MSVM \_ BindsToLANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1092f-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1092f-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1092f-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1092f-115">Tipo de datos: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="1092f-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1092f-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1092f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1092f-117">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="1092f-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1092f-118">Una referencia a una clase [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) que representa el puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="1092f-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="1092f-119">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="1092f-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="1092f-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1092f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1092f-121">Tipo de datos: **[ **MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="1092f-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1092f-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1092f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1092f-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="1092f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1092f-124">Una referencia a [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) asociada con el puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="1092f-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="1092f-125">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="1092f-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="1092f-126">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="1092f-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1092f-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1092f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1092f-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1092f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1092f-129">Describe el método de tramas para el punto de conexión o SAP de nivel superior que está enlazado al punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="1092f-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="1092f-130">Esta propiedad se hereda de **CIM \_ BindsToLANEndpoint** y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="1092f-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1092f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1092f-131">Requirements</span></span>



| <span data-ttu-id="1092f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1092f-132">Requirement</span></span> | <span data-ttu-id="1092f-133">Value</span><span class="sxs-lookup"><span data-stu-id="1092f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1092f-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1092f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1092f-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1092f-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1092f-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1092f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1092f-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1092f-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1092f-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1092f-138">Namespace</span></span><br/>                | <span data-ttu-id="1092f-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1092f-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1092f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1092f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1092f-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1092f-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1092f-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1092f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1092f-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1092f-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

