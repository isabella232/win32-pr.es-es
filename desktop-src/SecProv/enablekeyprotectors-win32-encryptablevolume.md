---
description: Habilita o reanuda todos los protectores de clave deshabilitados o suspendidos.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Método EnableKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686659"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="44e77-103">Método EnableKeyProtectors de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="44e77-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="44e77-104">El método **EnableKeyProtectors** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) habilita o reanuda todos los protectores de clave deshabilitados o suspendidos.</span><span class="sxs-lookup"><span data-stu-id="44e77-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="44e77-105">Puede usar este método para volver a habilitar o reanudar la protección de BitLocker en un volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="44e77-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="44e77-106">Este método garantiza que la clave de cifrado del volumen no se exponga en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="44e77-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="44e77-107">Si el disco es compatible con el cifrado de hardware, el estado de la banda cambia a "desbloqueado" de "siempre desbloqueado".</span><span class="sxs-lookup"><span data-stu-id="44e77-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44e77-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44e77-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="44e77-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44e77-109">Parameters</span></span>

<span data-ttu-id="44e77-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="44e77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44e77-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44e77-111">Return value</span></span>

<span data-ttu-id="44e77-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e77-112">Type: **uint32**</span></span>

<span data-ttu-id="44e77-113">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="44e77-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="44e77-114">Si los protectores de clave ya están habilitados y no se producen otros errores, este método devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="44e77-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44e77-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44e77-115">Return code/value</span></span></th>
<th><span data-ttu-id="44e77-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="44e77-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="44e77-117"><dt><strong>S_OK</strong></dt> <dt>0 (0X0)</dt> </span><span class="sxs-lookup"><span data-stu-id="44e77-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="44e77-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="44e77-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="44e77-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="44e77-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="44e77-120">No existe ningún protector de clave en el volumen.</span><span class="sxs-lookup"><span data-stu-id="44e77-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="44e77-121">Use uno de los métodos siguientes para especificar los protectores de clave para el volumen:</span><span class="sxs-lookup"><span data-stu-id="44e77-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="44e77-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="44e77-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="44e77-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="44e77-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="44e77-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="44e77-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="44e77-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="44e77-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="44e77-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="44e77-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="44e77-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="44e77-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="44e77-132">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="44e77-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="44e77-133">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="44e77-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="44e77-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44e77-134">Remarks</span></span>

<span data-ttu-id="44e77-135">Si el volumen está totalmente cifrado, la ejecución correcta de este método garantiza que el volumen esté protegido.</span><span class="sxs-lookup"><span data-stu-id="44e77-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="44e77-136">Si el volumen está parcialmente cifrado, la ejecución correcta de este método implica que el volumen se protegerá cuando se cifre completamente.</span><span class="sxs-lookup"><span data-stu-id="44e77-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="44e77-137">Para obtener más información, vea el método [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="44e77-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="44e77-138">Si existen protectores de clave basados en TPM para el volumen, al ejecutar correctamente este método también se actualizan estos protectores para que el TPM se valide con respecto a los servicios de inicio actuales en la plataforma.</span><span class="sxs-lookup"><span data-stu-id="44e77-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="44e77-139">En otras palabras, está afirmando que el estado actual del equipo es el correcto que el TPM comprobará en los reinicios futuros del equipo.</span><span class="sxs-lookup"><span data-stu-id="44e77-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="44e77-140">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="44e77-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44e77-141">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="44e77-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="44e77-142">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="44e77-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44e77-143">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="44e77-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44e77-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e77-144">Requirements</span></span>



| <span data-ttu-id="44e77-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e77-145">Requirement</span></span> | <span data-ttu-id="44e77-146">Value</span><span class="sxs-lookup"><span data-stu-id="44e77-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e77-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e77-147">Minimum supported client</span></span><br/> | <span data-ttu-id="44e77-148">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="44e77-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="44e77-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e77-149">Minimum supported server</span></span><br/> | <span data-ttu-id="44e77-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44e77-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44e77-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44e77-151">Namespace</span></span><br/>                | <span data-ttu-id="44e77-152">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="44e77-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="44e77-153">MOF</span><span class="sxs-lookup"><span data-stu-id="44e77-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44e77-154"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44e77-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e77-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="44e77-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e77-156">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="44e77-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-157">**DisableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="44e77-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-158">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="44e77-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-159">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="44e77-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-160">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="44e77-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-161">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="44e77-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-162">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="44e77-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-163">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="44e77-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-164">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="44e77-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="44e77-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="44e77-166">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="44e77-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
