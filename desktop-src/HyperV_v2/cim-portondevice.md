---
description: Representa una asociación entre un puerto o un punto de conexión y un dispositivo.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: CIM_PortOnDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670035"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="c7d9f-103">\_Clase PortOnDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="c7d9f-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="c7d9f-104">Representa una asociación entre un puerto o un punto de conexión y un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7d9f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c7d9f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7d9f-106">Members</span></span>

<span data-ttu-id="c7d9f-107">La clase **CIM \_ PortOnDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c7d9f-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c7d9f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7d9f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7d9f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7d9f-109">Properties</span></span>

<span data-ttu-id="c7d9f-110">La clase **CIM \_ PortOnDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7d9f-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c7d9f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7d9f-112">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="c7d9f-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c7d9f-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7d9f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7d9f-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="c7d9f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c7d9f-115">El dispositivo que incluye el puerto.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="c7d9f-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="c7d9f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7d9f-117">Tipo de datos: **CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="c7d9f-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="c7d9f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7d9f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7d9f-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="c7d9f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c7d9f-120">Puerto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7d9f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7d9f-121">Requirements</span></span>



| <span data-ttu-id="c7d9f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7d9f-122">Requirement</span></span> | <span data-ttu-id="c7d9f-123">Value</span><span class="sxs-lookup"><span data-stu-id="c7d9f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d9f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7d9f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d9f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7d9f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7d9f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7d9f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d9f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7d9f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7d9f-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7d9f-128">Namespace</span></span><br/>                | <span data-ttu-id="c7d9f-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c7d9f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7d9f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c7d9f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7d9f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7d9f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7d9f-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7d9f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7d9f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7d9f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7d9f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7d9f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d9f-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="c7d9f-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

