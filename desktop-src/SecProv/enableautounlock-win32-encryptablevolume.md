---
description: Permite que un volumen de datos se desbloquee automáticamente al montar el volumen.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Método EnableAutoUnlock de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910042"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d965c-103">Método EnableAutoUnlock de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d965c-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d965c-104">El método **EnableAutoUnlock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) permite que un volumen de datos se desbloquee automáticamente al montar el volumen.</span><span class="sxs-lookup"><span data-stu-id="d965c-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="d965c-105">El desbloqueo automático guarda una clave externa en el sistema operativo que puede desbloquear automáticamente el volumen en el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d965c-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="d965c-106">Para usar este método, el volumen del sistema operativo ya debe estar protegido por Cifrado de unidad BitLocker o debe tener cifrado en curso.</span><span class="sxs-lookup"><span data-stu-id="d965c-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="d965c-107">Además, ya debe existir una clave externa para el volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="d965c-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="d965c-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear la clave externa que puede desbloquear el volumen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d965c-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="d965c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d965c-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="d965c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d965c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d965c-111">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d965c-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d965c-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d965c-112">Type: **string**</span></span>

<span data-ttu-id="d965c-113">Cadena que identifica el protector de clave del tipo "clave externa" que se usa para desbloquear automáticamente el volumen.</span><span class="sxs-lookup"><span data-stu-id="d965c-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d965c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d965c-114">Return value</span></span>

<span data-ttu-id="d965c-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d965c-115">Type: **uint32**</span></span>

<span data-ttu-id="d965c-116">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d965c-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d965c-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d965c-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="d965c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d965c-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d965c-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="d965c-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d965c-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="d965c-121"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="d965c-122">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d965c-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="d965c-123"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="d965c-124">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d965c-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d965c-125">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d965c-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="d965c-126"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="d965c-127">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave válido del tipo "external key".</span><span class="sxs-lookup"><span data-stu-id="d965c-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="d965c-128"><dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="d965c-129">No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d965c-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="d965c-130"><dt>**FVE \_ E \_ so \_ no \_ protegido**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="d965c-131">El método no se puede ejecutar si el volumen del sistema operativo que se está ejecutando actualmente no está protegido por Cifrado de unidad BitLocker o no tiene cifrado en curso.</span><span class="sxs-lookup"><span data-stu-id="d965c-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="d965c-132"><dt> **FVE \_ E \_ \_ enlazado \_ por volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="d965c-133">El desbloqueo automático en el volumen se ha habilitado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d965c-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d965c-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d965c-134">Remarks</span></span>

<span data-ttu-id="d965c-135">Dado un protector de clave de volumen válido del tipo "clave externa", se extrae la clave externa de 256 bits relacionada del protector y se almacena en el registro del sistema operativo que se está ejecutando actualmente, junto con el identificador de protector de clave de volumen.</span><span class="sxs-lookup"><span data-stu-id="d965c-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="d965c-136">Si se elimina la clave externa asociada con el identificador de protector de clave de volumen, la funcionalidad para desbloquear el volumen automáticamente está deshabilitada o suspendida.</span><span class="sxs-lookup"><span data-stu-id="d965c-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="d965c-137">Los medios extraíbles no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="d965c-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="d965c-138">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d965c-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d965c-139">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d965c-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d965c-140">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d965c-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d965c-141">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d965c-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d965c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d965c-142">Requirements</span></span>



| <span data-ttu-id="d965c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d965c-143">Requirement</span></span> | <span data-ttu-id="d965c-144">Value</span><span class="sxs-lookup"><span data-stu-id="d965c-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d965c-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d965c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d965c-146">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d965c-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d965c-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d965c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d965c-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d965c-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d965c-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d965c-149">Namespace</span></span><br/>                | <span data-ttu-id="d965c-150">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d965c-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d965c-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d965c-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d965c-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d965c-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d965c-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="d965c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d965c-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d965c-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
