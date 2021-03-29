---
description: Indica si el volumen y su clave de cifrado están protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809283"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4aa4e-103">Método GetProtectionStatus de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="4aa4e-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4aa4e-104">El método **GetProtectionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen y su clave de cifrado (si existen) están protegidos.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="4aa4e-105">La protección está desactivada si un volumen no está cifrado o parcialmente cifrado, o si la clave de cifrado del volumen está disponible en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa4e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4aa4e-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4aa4e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4aa4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa4e-108">*ProtectionStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4aa4e-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa4e-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-109">Type: **uint32**</span></span>

<span data-ttu-id="4aa4e-110">Especifica si el volumen y la clave de cifrado (si existen) están protegidos.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4aa4e-111">Value</span><span class="sxs-lookup"><span data-stu-id="4aa4e-111">Value</span></span></th>
<th><span data-ttu-id="4aa4e-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4aa4e-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="4aa4e-113"><dt><strong>Desprotegido</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="4aa4e-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="4aa4e-114">PROTECCIÓN DESACTIVADA</span><span class="sxs-lookup"><span data-stu-id="4aa4e-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="4aa4e-115">Para una unidad de disco duro estándar:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-115">For a standard HDD:</span></span><br/> <span data-ttu-id="4aa4e-116">El volumen está sin cifrar, parcialmente cifrado o la clave de cifrado del volumen está disponible en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="4aa4e-117">La clave de cifrado está disponible en el disco duro sin cifrado si se han deshabilitado los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o si no se ha especificado ningún protector de clave mediante los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="4aa4e-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="4aa4e-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="4aa4e-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="4aa4e-127">Para un EHDD:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-127">For an EHDD:</span></span><br/> <span data-ttu-id="4aa4e-128">La banda del volumen se desbloquea perpetuamente, no tiene administrador de claves o está administrada por un administrador de claves de terceros.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="4aa4e-129">Esto también puede significar que la banda está administrada por BitLocker, pero se ha llamado al método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> y la unidad está suspendida.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="4aa4e-130"><dt><strong>Protegido</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="4aa4e-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="4aa4e-131">PROTECCIÓN ACTIVADA</span><span class="sxs-lookup"><span data-stu-id="4aa4e-131">PROTECTION ON</span></span><br/> <span data-ttu-id="4aa4e-132">Para una unidad de disco duro estándar:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-132">For a standard HDD:</span></span><br/> <span data-ttu-id="4aa4e-133">El volumen está totalmente cifrado y la clave de cifrado del volumen no está disponible en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="4aa4e-134">Para un EHDD:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-134">For an EHDD:</span></span><br/> <span data-ttu-id="4aa4e-135">BitLocker es el administrador de claves de la banda.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="4aa4e-136">La unidad puede estar bloqueada o desbloqueada, pero no se puede desbloquear perpetuamente.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4aa4e-137"><dt><strong>Desconocido</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="4aa4e-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="4aa4e-138">No se puede determinar el estado de protección del volumen.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="4aa4e-139">Esto puede deberse a que el volumen está en estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="4aa4e-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise y Windows Server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="4aa4e-141">Este valor se admite a partir de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa4e-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aa4e-142">Return value</span></span>

<span data-ttu-id="4aa4e-143">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-143">Type: **uint32**</span></span>

<span data-ttu-id="4aa4e-144">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4aa4e-145">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aa4e-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4aa4e-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="4aa4e-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4aa4e-147"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="4aa4e-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4aa4e-148">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4aa4e-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4aa4e-149">Remarks</span></span>

<span data-ttu-id="4aa4e-150">Solo se puede cifrar un volumen si se llama a [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) en primer lugar o se usa uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="4aa4e-151">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-152">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-153">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-154">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-155">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-156">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-157">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="4aa4e-159">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="4aa4e-160">Por lo tanto, si el disco está cifrado y *ProtectionStatus* devuelve cero (protección desactivada), se deshabilitan las claves.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="4aa4e-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) para enumerar los protectores de clave especificados para proteger la clave de cifrado del volumen.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="4aa4e-162">Si existen protectores de clave pero la protección es cero (protección desactivada), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para activar la protección del volumen.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="4aa4e-163">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4aa4e-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4aa4e-164">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4aa4e-165">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4aa4e-166">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4aa4e-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa4e-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aa4e-167">Requirements</span></span>



| <span data-ttu-id="4aa4e-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa4e-168">Requirement</span></span> | <span data-ttu-id="4aa4e-169">Value</span><span class="sxs-lookup"><span data-stu-id="4aa4e-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa4e-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4aa4e-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa4e-171">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="4aa4e-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4aa4e-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4aa4e-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa4e-173">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4aa4e-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4aa4e-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4aa4e-174">Namespace</span></span><br/>                | <span data-ttu-id="4aa4e-175">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="4aa4e-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4aa4e-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4aa4e-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aa4e-177"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aa4e-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa4e-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aa4e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa4e-179">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4aa4e-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
