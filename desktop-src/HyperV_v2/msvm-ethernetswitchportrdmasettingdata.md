---
description: Representa los datos de configuración de la característica RDMA de puerto.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Msvm_EthernetSwitchPortRdmaSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913890"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="a0f91-103">MSVM \_ EthernetSwitchPortRdmaSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="a0f91-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="a0f91-104">Representa los datos de configuración de la característica RDMA de puerto.</span><span class="sxs-lookup"><span data-stu-id="a0f91-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="a0f91-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0f91-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f91-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0f91-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="a0f91-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0f91-107">Members</span></span>

<span data-ttu-id="a0f91-108">La clase **MSVM \_ EthernetSwitchPortRdmaSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0f91-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a0f91-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0f91-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0f91-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0f91-110">Properties</span></span>

<span data-ttu-id="a0f91-111">La clase **MSVM \_ EthernetSwitchPortRdmaSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0f91-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0f91-112">**RdmaOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="a0f91-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0f91-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0f91-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0f91-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0f91-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0f91-115">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a0f91-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a0f91-116">El peso asignado a este puerto para el RDMA invitado.</span><span class="sxs-lookup"><span data-stu-id="a0f91-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="a0f91-117">El peso es la importancia relativa al asignar recursos RDMA.</span><span class="sxs-lookup"><span data-stu-id="a0f91-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="a0f91-118">Al establecer la propiedad **RdmaOffloadWeight** en 0, se deshabilita RDMA en el puerto.</span><span class="sxs-lookup"><span data-stu-id="a0f91-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="a0f91-119">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="a0f91-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0f91-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f91-120">Requirements</span></span>



| <span data-ttu-id="a0f91-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f91-121">Requirement</span></span> | <span data-ttu-id="a0f91-122">Value</span><span class="sxs-lookup"><span data-stu-id="a0f91-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f91-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0f91-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f91-124">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0f91-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a0f91-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0f91-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f91-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a0f91-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a0f91-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0f91-127">Namespace</span></span><br/>                | <span data-ttu-id="a0f91-128">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0f91-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a0f91-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a0f91-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0f91-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0f91-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0f91-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0f91-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0f91-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0f91-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0f91-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0f91-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f91-134">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="a0f91-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




