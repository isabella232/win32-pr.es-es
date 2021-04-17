---
description: Representa la configuración de descarga del conmutador.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Msvm_EthernetSwitchHardwareOffloadSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689588"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="f51e2-103">MSVM \_ EthernetSwitchHardwareOffloadSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="f51e2-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="f51e2-104">Representa la configuración de descarga del conmutador.</span><span class="sxs-lookup"><span data-stu-id="f51e2-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="f51e2-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f51e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51e2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f51e2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="f51e2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f51e2-107">Members</span></span>

<span data-ttu-id="f51e2-108">La clase **MSVM \_ EthernetSwitchHardwareOffloadSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f51e2-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f51e2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f51e2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f51e2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f51e2-110">Properties</span></span>

<span data-ttu-id="f51e2-111">La clase **MSVM \_ EthernetSwitchHardwareOffloadSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f51e2-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f51e2-112">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="f51e2-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f51e2-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f51e2-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-115">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-116">Especifica la configuración de VMMQ para la cola predeterminada del vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f51e2-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="f51e2-117">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="f51e2-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f51e2-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f51e2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-120">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-121">Especifica el número de colas para la cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f51e2-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="f51e2-122">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="f51e2-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f51e2-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f51e2-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-125">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-126">Especifica la configuración de VRss para la cola predeterminada del vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f51e2-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="f51e2-127">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="f51e2-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f51e2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f51e2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-130">Calificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-131">Indica si la CPU VMQ primaria está excluida de la tabla de indirección VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="f51e2-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="f51e2-132">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f51e2-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f51e2-133">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="f51e2-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f51e2-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f51e2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-136">Calificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-137">Indica si se va a realizar siempre la propagación de VRSS para la cola predeterminada, independientemente del estado de RSS del vPort externo.</span><span class="sxs-lookup"><span data-stu-id="f51e2-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="f51e2-138">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f51e2-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f51e2-139">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="f51e2-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f51e2-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f51e2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-142">Calificadores: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-143">Indica el número mínimo de colas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="f51e2-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="f51e2-144">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f51e2-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f51e2-145">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="f51e2-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f51e2-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f51e2-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f51e2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f51e2-148">Calificadores: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f51e2-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f51e2-149">Indica cómo se dirigen las colas de VRSS/VMMQ a diferentes procesadores de host.</span><span class="sxs-lookup"><span data-stu-id="f51e2-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="f51e2-150">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f51e2-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f51e2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51e2-151">Requirements</span></span>



| <span data-ttu-id="f51e2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51e2-152">Requirement</span></span> | <span data-ttu-id="f51e2-153">Value</span><span class="sxs-lookup"><span data-stu-id="f51e2-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e2-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51e2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f51e2-155">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f51e2-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f51e2-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51e2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f51e2-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f51e2-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f51e2-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f51e2-158">Namespace</span></span><br/>                | <span data-ttu-id="f51e2-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f51e2-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f51e2-160">MOF</span><span class="sxs-lookup"><span data-stu-id="f51e2-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f51e2-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f51e2-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f51e2-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f51e2-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51e2-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f51e2-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f51e2-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="f51e2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51e2-165">**MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="f51e2-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




