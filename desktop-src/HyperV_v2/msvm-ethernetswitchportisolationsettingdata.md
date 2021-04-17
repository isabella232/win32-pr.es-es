---
description: Representa los datos de configuración de aislamiento.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667683"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="35518-103">MSVM \_ EthernetSwitchPortIsolationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="35518-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="35518-104">Representa los datos de configuración de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="35518-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="35518-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35518-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35518-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35518-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="35518-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35518-107">Members</span></span>

<span data-ttu-id="35518-108">La clase **MSVM \_ EthernetSwitchPortIsolationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35518-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="35518-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35518-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35518-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35518-110">Properties</span></span>

<span data-ttu-id="35518-111">La clase **MSVM \_ EthernetSwitchPortIsolationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35518-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35518-112">**AllowUntaggedTraffic**</span><span class="sxs-lookup"><span data-stu-id="35518-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35518-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="35518-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35518-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35518-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35518-115">Calificadores: **WmiDataId** (2), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="35518-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="35518-116">Si el puerto puede enviar o recibir tráfico sin etiquetar.</span><span class="sxs-lookup"><span data-stu-id="35518-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="35518-117">**DefaultIsolationId**</span><span class="sxs-lookup"><span data-stu-id="35518-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35518-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35518-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35518-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35518-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35518-120">Calificadores: **WmiDataId** (3), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="35518-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="35518-121">La VirtualSubnetId o VLAN predeterminada que se establecerá en todo el tráfico de envío y recepción si **AllowedUntaggedTraffic** es **true**.</span><span class="sxs-lookup"><span data-stu-id="35518-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="35518-122">**EnableMultiTenantStack**</span><span class="sxs-lookup"><span data-stu-id="35518-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35518-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="35518-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35518-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35518-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35518-125">Calificadores: **WmiDataId** (4), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="35518-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="35518-126">Si **es true**, la pila de red de la máquina virtual podrá tener acceso a la configuración de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="35518-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="35518-127">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="35518-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="35518-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="35518-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35518-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35518-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35518-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35518-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35518-131">Calificadores: **WmiDataId** (1), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="35518-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="35518-132">Si el puerto usa **VLAN** o **VirtualSubnetId** para el aislamiento.</span><span class="sxs-lookup"><span data-stu-id="35518-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="35518-133">**NativeVirtualSubnetId** se usa para redes basadas en WNV VirtualSubnetId.</span><span class="sxs-lookup"><span data-stu-id="35518-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="35518-134">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="35518-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="35518-135">**NativeVirtualSubnetId** (1)</span><span class="sxs-lookup"><span data-stu-id="35518-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="35518-136">**ExternalVirtualSubnetId** (2)</span><span class="sxs-lookup"><span data-stu-id="35518-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="35518-137">**VLAN** (3)</span><span class="sxs-lookup"><span data-stu-id="35518-137">**VLAN** (3)</span></span>


<span data-ttu-id="35518-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="35518-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="35518-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35518-139">Requirements</span></span>



| <span data-ttu-id="35518-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="35518-140">Requirement</span></span> | <span data-ttu-id="35518-141">Value</span><span class="sxs-lookup"><span data-stu-id="35518-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35518-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35518-142">Minimum supported client</span></span><br/> | <span data-ttu-id="35518-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="35518-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="35518-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35518-144">Minimum supported server</span></span><br/> | <span data-ttu-id="35518-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="35518-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="35518-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35518-146">Namespace</span></span><br/>                | <span data-ttu-id="35518-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="35518-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35518-148">MOF</span><span class="sxs-lookup"><span data-stu-id="35518-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35518-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35518-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35518-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35518-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35518-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35518-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35518-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="35518-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35518-153">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="35518-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

