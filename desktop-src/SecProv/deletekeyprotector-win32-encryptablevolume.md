---
description: Elimina un protector de clave determinado para el volumen.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Método DeleteKeyProtector de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360214"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d691d-103">Método DeleteKeyProtector de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d691d-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d691d-104">El método **DeleteKeyProtector** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina un protector de clave determinado para el volumen.</span><span class="sxs-lookup"><span data-stu-id="d691d-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="d691d-105">Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtector** quita el último protector de clave, el volumen se revierte a un sistema de archivos NTFS estándar.</span><span class="sxs-lookup"><span data-stu-id="d691d-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="d691d-106">Si nunca se ha cifrado un volumen, la eliminación del protector de clave revertirá a NTFS.</span><span class="sxs-lookup"><span data-stu-id="d691d-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="d691d-107">Si el volumen no se ha descifrado por completo, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar el último protector de clave del volumen para asegurarse de que las partes cifradas del volumen sigan siendo accesibles.</span><span class="sxs-lookup"><span data-stu-id="d691d-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="d691d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d691d-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="d691d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d691d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d691d-110">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d691d-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d691d-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d691d-111">Type: **string**</span></span>

<span data-ttu-id="d691d-112">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="d691d-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d691d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d691d-113">Return value</span></span>

<span data-ttu-id="d691d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d691d-114">Type: **uint32**</span></span>

<span data-ttu-id="d691d-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d691d-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d691d-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d691d-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d691d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d691d-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d691d-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="d691d-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d691d-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d691d-120"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="d691d-121">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d691d-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d691d-122"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="d691d-123">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d691d-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d691d-124">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d691d-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d691d-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="d691d-126">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave válido.</span><span class="sxs-lookup"><span data-stu-id="d691d-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d691d-127"><dt>**FVE \_ E \_ clave \_ necesaria**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="d691d-128">No se puede quitar el último protector de clave para un volumen totalmente cifrado o parcial si están habilitados los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="d691d-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="d691d-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar este protector de clave más reciente para asegurarse de que las partes cifradas del volumen sigan siendo accesibles.</span><span class="sxs-lookup"><span data-stu-id="d691d-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="d691d-130"><dt>**FVE \_ E \_ \_ enlazado \_ a un volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="d691d-131">Este protector de clave no se puede eliminar porque se está usando para desbloquear automáticamente el volumen.</span><span class="sxs-lookup"><span data-stu-id="d691d-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="d691d-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para deshabilitar el desbloqueo automático antes de eliminar este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="d691d-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d691d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d691d-133">Remarks</span></span>

<span data-ttu-id="d691d-134">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d691d-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d691d-135">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d691d-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d691d-136">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d691d-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d691d-137">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d691d-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d691d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d691d-138">Requirements</span></span>



| <span data-ttu-id="d691d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d691d-139">Requirement</span></span> | <span data-ttu-id="d691d-140">Value</span><span class="sxs-lookup"><span data-stu-id="d691d-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d691d-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d691d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d691d-142">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d691d-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d691d-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d691d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d691d-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d691d-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d691d-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d691d-145">Namespace</span></span><br/>                | <span data-ttu-id="d691d-146">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d691d-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d691d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d691d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d691d-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d691d-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d691d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d691d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d691d-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d691d-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
