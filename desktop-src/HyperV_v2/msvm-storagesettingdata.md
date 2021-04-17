---
description: Representa la configuración específica del almacenamiento para un sistema virtual.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653093"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="358fb-103">MSVM \_ StorageSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="358fb-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="358fb-104">Representa la configuración específica del almacenamiento para un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="358fb-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="358fb-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="358fb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="358fb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="358fb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="358fb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="358fb-107">Members</span></span>

<span data-ttu-id="358fb-108">La clase **MSVM \_ StorageSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="358fb-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="358fb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="358fb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="358fb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="358fb-110">Properties</span></span>

<span data-ttu-id="358fb-111">La clase **MSVM \_ StorageSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="358fb-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="358fb-112">**DisableInterruptBatching**</span><span class="sxs-lookup"><span data-stu-id="358fb-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="358fb-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="358fb-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="358fb-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="358fb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="358fb-115">Especifica si el procesamiento por lotes de interrupción debe deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="358fb-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="358fb-116">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**\_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) de WMI MSVM.</span><span class="sxs-lookup"><span data-stu-id="358fb-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="358fb-117">**ThreadCountPerChannel**</span><span class="sxs-lookup"><span data-stu-id="358fb-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="358fb-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="358fb-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="358fb-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="358fb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="358fb-120">El número de subprocesos por canal de almacenamiento para procesar la e/s.</span><span class="sxs-lookup"><span data-stu-id="358fb-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="358fb-121">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="358fb-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="358fb-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="358fb-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="358fb-123">Comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="358fb-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="358fb-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (1)</span><span class="sxs-lookup"><span data-stu-id="358fb-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="358fb-125">Número bajo de subprocesos por canal de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="358fb-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="358fb-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medio** (2)</span><span class="sxs-lookup"><span data-stu-id="358fb-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="358fb-127">Número medio de subprocesos por canal de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="358fb-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="358fb-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)</span><span class="sxs-lookup"><span data-stu-id="358fb-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="358fb-129">Gran número de subprocesos por canal de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="358fb-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="358fb-130">**VirtualProcessorsPerChannel**</span><span class="sxs-lookup"><span data-stu-id="358fb-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="358fb-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="358fb-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="358fb-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="358fb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="358fb-133">El número de procesadores por canal de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="358fb-133">The number of processors per storage channel.</span></span> <span data-ttu-id="358fb-134">El número de canales que se van a abrir viene dado por (recuento de procesadores lógicos en el host/**VirtualProcessorsPerChannel**).</span><span class="sxs-lookup"><span data-stu-id="358fb-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="358fb-135">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="358fb-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="358fb-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="358fb-136">Requirements</span></span>



| <span data-ttu-id="358fb-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="358fb-137">Requirement</span></span> | <span data-ttu-id="358fb-138">Value</span><span class="sxs-lookup"><span data-stu-id="358fb-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="358fb-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="358fb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="358fb-140">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="358fb-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="358fb-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="358fb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="358fb-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="358fb-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="358fb-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="358fb-143">Namespace</span></span><br/>                | <span data-ttu-id="358fb-144">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="358fb-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="358fb-145">MOF</span><span class="sxs-lookup"><span data-stu-id="358fb-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="358fb-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="358fb-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="358fb-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="358fb-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="358fb-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="358fb-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="358fb-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="358fb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358fb-150">**MSVM \_ SystemComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="358fb-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




