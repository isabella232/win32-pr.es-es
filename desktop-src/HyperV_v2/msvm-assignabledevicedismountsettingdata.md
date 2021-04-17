---
description: Representa la configuración de un sistema virtual que se va a importar. Lo usa el método Dismount de la \_ clase MSVM AssignableDeviceService.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Msvm_AssignableDeviceDismountSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667830"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="7b6ad-104">MSVM \_ AssignableDeviceDismountSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="7b6ad-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="7b6ad-105">Representa la configuración de un sistema virtual que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="7b6ad-106">Lo usa el método [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) de la clase [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7b6ad-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="7b6ad-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6ad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b6ad-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="7b6ad-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b6ad-109">Members</span></span>

<span data-ttu-id="7b6ad-110">La clase **MSVM \_ AssignableDeviceDismountSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b6ad-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b6ad-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b6ad-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b6ad-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b6ad-112">Properties</span></span>

<span data-ttu-id="7b6ad-113">La clase **MSVM \_ AssignableDeviceDismountSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b6ad-114">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ad-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ad-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b6ad-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ad-117">IDENTIFICADOR de instancia del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ad-118">**DeviceLocationPath**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ad-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ad-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b6ad-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ad-121">Ruta de acceso de ubicación del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ad-122">**RequireAcsSupport**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ad-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ad-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b6ad-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ad-125">Indica si la compatibilidad con ACS necesaria debe estar en su lugar antes de permitir el desmontaje.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ad-126">**RequireDeviceMitigations**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ad-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ad-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b6ad-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ad-129">Indica si deben aplicarse mitigaciones de dispositivo antes de permitir el desmontaje.</span><span class="sxs-lookup"><span data-stu-id="7b6ad-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b6ad-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b6ad-130">Requirements</span></span>



| <span data-ttu-id="7b6ad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b6ad-131">Requirement</span></span> | <span data-ttu-id="7b6ad-132">Value</span><span class="sxs-lookup"><span data-stu-id="7b6ad-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6ad-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b6ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6ad-134">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b6ad-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b6ad-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b6ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6ad-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b6ad-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7b6ad-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b6ad-137">Namespace</span></span><br/>                | <span data-ttu-id="7b6ad-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7b6ad-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b6ad-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7b6ad-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b6ad-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b6ad-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b6ad-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b6ad-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b6ad-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b6ad-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b6ad-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b6ad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6ad-144">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7b6ad-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




