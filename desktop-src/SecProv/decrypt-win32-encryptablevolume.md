---
description: Inicia el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método de descifrado de la clase Win32_EncryptableVolume (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910054"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f2e29-103">Método de descifrado de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="f2e29-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f2e29-104">El método de **descifrado** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inicia el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="f2e29-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="f2e29-105">Cuando el descifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="f2e29-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="f2e29-106">Cuando el cifrado está en pausa o en curso, este método revierte el cifrado y comienza el descifrado.</span><span class="sxs-lookup"><span data-stu-id="f2e29-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="f2e29-107">Una vez completado el descifrado, todos los protectores de clave de este volumen se quitan del sistema y el volumen se convierte en un sistema de archivos NTFS estándar.</span><span class="sxs-lookup"><span data-stu-id="f2e29-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="f2e29-108">Si el disco está cifrado por hardware, el método de **descifrado** establece el estado de la banda en "siempre desbloqueado", quita todos los metadatos asociados y pone a cero el ID. de seguridad de la unidad.</span><span class="sxs-lookup"><span data-stu-id="f2e29-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f2e29-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2e29-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="f2e29-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2e29-110">Parameters</span></span>

<span data-ttu-id="f2e29-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f2e29-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2e29-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2e29-112">Return value</span></span>

<span data-ttu-id="f2e29-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2e29-113">Type: **uint32**</span></span>

<span data-ttu-id="f2e29-114">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f2e29-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="f2e29-115">Este método vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2e29-115">This method returns immediately.</span></span> <span data-ttu-id="f2e29-116">Si el volumen ya está completamente descifrado y no existe ningún otro error, este método devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="f2e29-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="f2e29-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2e29-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f2e29-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2e29-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2e29-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e29-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="f2e29-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2e29-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="f2e29-121"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e29-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="f2e29-122">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f2e29-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f2e29-123"><dt>**FVE \_ E \_ DESbloqueo automático \_ habilitado**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e29-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="f2e29-124">Este volumen no se puede descifrar porque están disponibles las claves usadas para desbloquear automáticamente los volúmenes de datos.</span><span class="sxs-lookup"><span data-stu-id="f2e29-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="f2e29-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para quitar estas claves.</span><span class="sxs-lookup"><span data-stu-id="f2e29-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="f2e29-126">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="f2e29-126">Security Considerations</span></span>

<span data-ttu-id="f2e29-127">La llamada al método **Decrypt** deja los datos desprotegidos.</span><span class="sxs-lookup"><span data-stu-id="f2e29-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="f2e29-128">Si el estado de protección del volumen es 1 (protección activada) antes de que se use este método, la finalización correcta de este método cambia el estado de protección a 0 (protección desactivada), ya que, por definición, un volumen parcialmente cifrado no está protegido.</span><span class="sxs-lookup"><span data-stu-id="f2e29-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e29-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2e29-129">Remarks</span></span>

<span data-ttu-id="f2e29-130">Si el volumen no se ha descifrado por completo, al ejecutar **descifrado** , [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indica que el descifrado es Progress y muestra el porcentaje del volumen que permanece cifrado.</span><span class="sxs-lookup"><span data-stu-id="f2e29-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="f2e29-131">Si el estado de protección del volumen es "activado" antes de que se ejecute este método, la ejecución de este método cambia el estado de protección a "desactivado", ya que, por definición, un volumen parcialmente cifrado no está protegido.</span><span class="sxs-lookup"><span data-stu-id="f2e29-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="f2e29-132">Si este método se ejecuta en el volumen del sistema operativo que se está ejecutando actualmente y se usa este volumen del sistema operativo para desbloquear automáticamente los volúmenes de datos (consulte el método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), primero debe llamar al método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="f2e29-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="f2e29-133">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f2e29-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f2e29-134">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f2e29-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f2e29-135">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f2e29-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f2e29-136">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f2e29-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e29-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e29-137">Requirements</span></span>



| <span data-ttu-id="f2e29-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e29-138">Requirement</span></span> | <span data-ttu-id="f2e29-139">Value</span><span class="sxs-lookup"><span data-stu-id="f2e29-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e29-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e29-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e29-141">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2e29-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f2e29-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e29-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e29-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2e29-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2e29-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2e29-144">Namespace</span></span><br/>                | <span data-ttu-id="f2e29-145">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="f2e29-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f2e29-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2e29-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e29-147"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e29-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="f2e29-148">MOF</span><span class="sxs-lookup"><span data-stu-id="f2e29-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2e29-149"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2e29-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e29-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2e29-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e29-151">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f2e29-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
