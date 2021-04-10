---
description: Representa la configuración del servicio de comunicación invitado.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Msvm_GuestCommunicationServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154597"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="cd511-103">MSVM \_ GuestCommunicationServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="cd511-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="cd511-104">Representa la configuración del servicio de comunicación invitado.</span><span class="sxs-lookup"><span data-stu-id="cd511-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="cd511-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd511-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd511-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd511-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="cd511-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd511-107">Members</span></span>

<span data-ttu-id="cd511-108">La clase **MSVM \_ GuestCommunicationServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd511-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cd511-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd511-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd511-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd511-110">Properties</span></span>

<span data-ttu-id="cd511-111">La clase **MSVM \_ GuestCommunicationServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd511-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd511-112">**EnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="cd511-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd511-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd511-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd511-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cd511-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cd511-115">EnabledStatePolicy es una enumeración de enteros que indica el estado habilitado, deshabilitado o predeterminado de **MSVM \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="cd511-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cd511-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="cd511-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd511-117">El servicio de comunicación se establece en el estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="cd511-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cd511-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cd511-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cd511-119">El servicio de comunicación se establece en el Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cd511-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="cd511-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="cd511-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cd511-121">El estado del servicio de comunicación depende de **DefaultEnabledStatePolicy** en **MSVM \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="cd511-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd511-122">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cd511-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd511-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd511-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd511-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd511-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd511-125">GUID del servicio.</span><span class="sxs-lookup"><span data-stu-id="cd511-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd511-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd511-126">Requirements</span></span>



| <span data-ttu-id="cd511-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd511-127">Requirement</span></span> | <span data-ttu-id="cd511-128">Value</span><span class="sxs-lookup"><span data-stu-id="cd511-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd511-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd511-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cd511-130">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd511-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cd511-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd511-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cd511-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cd511-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cd511-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd511-133">Namespace</span></span><br/>                | <span data-ttu-id="cd511-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cd511-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd511-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cd511-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd511-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd511-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd511-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd511-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd511-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd511-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd511-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd511-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd511-140">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cd511-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




