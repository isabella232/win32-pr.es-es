---
title: MDM_BitLocker (clase)
description: '\_La empresa usa la clase BitLocker de MDM para administrar el cifrado de equipos y dispositivos.'
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- MDM_BitLocker (clase)
- MDM_BitLocker clase, descrita
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151105"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="fc09f-105">Clase de BitLocker de MDM \_</span><span class="sxs-lookup"><span data-stu-id="fc09f-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="fc09f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fc09f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fc09f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fc09f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fc09f-108">\_La empresa usa la clase BitLocker de MDM para administrar el cifrado de equipos y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fc09f-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="fc09f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fc09f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc09f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc09f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="fc09f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc09f-111">Members</span></span>

<span data-ttu-id="fc09f-112">La clase de **\_ BitLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc09f-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="fc09f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc09f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc09f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc09f-114">Properties</span></span>

<span data-ttu-id="fc09f-115">La clase de **\_ BitLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc09f-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fc09f-116">AllowWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fc09f-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fc09f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-119">EncryptionMethodByDriveType</span><span class="sxs-lookup"><span data-stu-id="fc09f-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-122">FixedDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="fc09f-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="fc09f-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc09f-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc09f-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc09f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fc09f-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc09f-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fc09f-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc09f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fc09f-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="fc09f-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="fc09f-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-140">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fc09f-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-142">RequireStorageCardEncryption</span><span class="sxs-lookup"><span data-stu-id="fc09f-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-143">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fc09f-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-145">SystemDrivesMinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="fc09f-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-148">SystemDrivesRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="fc09f-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-151">SystemDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="fc09f-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fc09f-154">SystemDrivesRequireStartupAuthentication</span><span class="sxs-lookup"><span data-stu-id="fc09f-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc09f-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc09f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc09f-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc09f-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc09f-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc09f-157">Requirements</span></span>



| <span data-ttu-id="fc09f-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc09f-158">Requirement</span></span> | <span data-ttu-id="fc09f-159">Value</span><span class="sxs-lookup"><span data-stu-id="fc09f-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc09f-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc09f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="fc09f-161">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc09f-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc09f-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc09f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="fc09f-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc09f-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="fc09f-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc09f-164">Namespace</span></span><br/>                | <span data-ttu-id="fc09f-165">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="fc09f-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="fc09f-166">MOF</span><span class="sxs-lookup"><span data-stu-id="fc09f-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc09f-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc09f-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc09f-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc09f-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc09f-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc09f-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

