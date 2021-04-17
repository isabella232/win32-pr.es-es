---
description: Representa el estado configurado de la configuración de seguridad para.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687629"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="98d4a-103">MSVM \_ SecuritySettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="98d4a-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="98d4a-104">Representa el estado configurado de la configuración de seguridad de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d4a-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="98d4a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="98d4a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d4a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98d4a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="98d4a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="98d4a-107">Members</span></span>

<span data-ttu-id="98d4a-108">La clase **MSVM \_ SecuritySettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="98d4a-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="98d4a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98d4a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98d4a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98d4a-110">Properties</span></span>

<span data-ttu-id="98d4a-111">La clase **MSVM \_ SecuritySettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="98d4a-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98d4a-112">**DataProtectionRequested**</span><span class="sxs-lookup"><span data-stu-id="98d4a-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-115">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-116">**true** para solicitar protección de datos para una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-117">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="98d4a-118">**EncryptStateAndVmMigrationTraffic**</span><span class="sxs-lookup"><span data-stu-id="98d4a-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-121">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-122">**true** para que el estado y el tráfico de migración de una máquina virtual estén cifrados; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-123">El valor predeterminado de una máquina virtual recién creada es **falso**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="98d4a-124">**KsdEnabled**</span><span class="sxs-lookup"><span data-stu-id="98d4a-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-127">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-128">**true** para habilitar un dispositivo de almacenamiento de claves (KSD) para esta máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-129">Una máquina virtual recién creada tiene deshabilitada la KSD.</span><span class="sxs-lookup"><span data-stu-id="98d4a-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="98d4a-130">**ShieldingRequested**</span><span class="sxs-lookup"><span data-stu-id="98d4a-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-133">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-134">**true** para solicitar el blindaje de una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-135">Una máquina virtual recién creada tiene un estado de blindaje solicitado de **falso**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="98d4a-136">**TpmEnabled**</span><span class="sxs-lookup"><span data-stu-id="98d4a-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-139">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-140">**true** para habilitar un Nodule de plataforma segura (TPM) para esta máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-141">Una máquina virtual recién creada tiene deshabilitado TPM.</span><span class="sxs-lookup"><span data-stu-id="98d4a-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="98d4a-142">**VirtualizationBasedSecurityOptOut**</span><span class="sxs-lookup"><span data-stu-id="98d4a-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d4a-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="98d4a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98d4a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98d4a-145">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98d4a-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98d4a-146">**true** para no ofrecer una seguridad basada en la virtualización de máquinas virtuales; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="98d4a-147">La configuración predeterminada para el estado de cancelación de una máquina virtual recién creada es **false**.</span><span class="sxs-lookup"><span data-stu-id="98d4a-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98d4a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d4a-148">Requirements</span></span>



| <span data-ttu-id="98d4a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d4a-149">Requirement</span></span> | <span data-ttu-id="98d4a-150">Value</span><span class="sxs-lookup"><span data-stu-id="98d4a-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d4a-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98d4a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="98d4a-152">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="98d4a-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98d4a-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98d4a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="98d4a-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="98d4a-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="98d4a-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98d4a-155">Namespace</span></span><br/>                | <span data-ttu-id="98d4a-156">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="98d4a-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="98d4a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="98d4a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98d4a-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98d4a-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98d4a-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98d4a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98d4a-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98d4a-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98d4a-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="98d4a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d4a-162">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="98d4a-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

