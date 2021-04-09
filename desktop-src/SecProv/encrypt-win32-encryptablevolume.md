---
description: Inicia el cifrado de un volumen totalmente descifrado o reanuda el cifrado de un volumen parcialmente cifrado.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Método Encrypt de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083342"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5e86c-103">Método Encrypt de la \_ clase Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5e86c-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5e86c-104">El método **Encrypt** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inicia el cifrado de un volumen totalmente descifrado o reanuda el cifrado de un volumen parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="5e86c-105">Cuando el cifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="5e86c-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="5e86c-106">Cuando el descifrado está en pausa o en curso, este método detiene el descifrado y comienza el cifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="5e86c-107">Si la unidad está cifrada por hardware, este método no cifra los datos.</span><span class="sxs-lookup"><span data-stu-id="5e86c-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="5e86c-108">En su lugar, establece el estado de la banda en "desbloqueado" de "siempre desbloqueado".</span><span class="sxs-lookup"><span data-stu-id="5e86c-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="5e86c-109">Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.</span><span class="sxs-lookup"><span data-stu-id="5e86c-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="5e86c-110">**Windows Vista:** No se admite el cifrado de un volumen distinto del volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="5e86c-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e86c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e86c-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5e86c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e86c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e86c-113">*EncryptionMethod* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5e86c-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e86c-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86c-114">Type: **uint32**</span></span>

<span data-ttu-id="5e86c-115">Entero sin signo que especifica el algoritmo de cifrado y el tamaño de la clave que se usa para cifrar el volumen.</span><span class="sxs-lookup"><span data-stu-id="5e86c-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="5e86c-116">Si este parámetro es mayor que cero y el volumen se ha cifrado parcial o totalmente, *EncryptionMethod* debe coincidir con el método de cifrado existente del volumen.</span><span class="sxs-lookup"><span data-stu-id="5e86c-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="5e86c-117">Si este parámetro es mayor que cero y el valor de directiva de grupo correspondiente está habilitado con un valor válido, *EncryptionMethod* debe coincidir con la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5e86c-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="5e86c-118">Para obtener una lista de posibles valores de EncryptionMethod, consulte el método [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="5e86c-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="5e86c-119">El valor predeterminado para Windows 7 o inferior es: 1 (AES \_ 128 \_ con \_ difusor).</span><span class="sxs-lookup"><span data-stu-id="5e86c-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="5e86c-120">El valor predeterminado para Windows 8, Windows 8.1 o Windows 10, versión 1507 es: 3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="5e86c-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="5e86c-121">El valor predeterminado de Windows 10, versión 1511 o superior es: 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="5e86c-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="5e86c-122">*EncryptionFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5e86c-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e86c-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86c-123">Type: **uint32**</span></span>

<span data-ttu-id="5e86c-124">Marcas que describen el comportamiento de cifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="5e86c-125">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise y Windows server 2008:** Este parámetro no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5e86c-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="5e86c-126">Combinación de 32 bits con los siguientes bits definidos actualmente.</span><span class="sxs-lookup"><span data-stu-id="5e86c-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="5e86c-127">Value</span><span class="sxs-lookup"><span data-stu-id="5e86c-127">Value</span></span>                                                                                  | <span data-ttu-id="5e86c-128">Significado</span><span class="sxs-lookup"><span data-stu-id="5e86c-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e86c-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5e86c-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="5e86c-130">Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="5e86c-131">Si el cifrado se ha pausado o detenido, la llamada al método de **cifrado** reanuda de forma eficaz la conversión y se omite el valor de este bit.</span><span class="sxs-lookup"><span data-stu-id="5e86c-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="5e86c-132">Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="5e86c-133">Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.</span><span class="sxs-lookup"><span data-stu-id="5e86c-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="5e86c-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5e86c-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="5e86c-135">Realice un borrado a petición del espacio libre del volumen.</span><span class="sxs-lookup"><span data-stu-id="5e86c-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="5e86c-136">Solo se permite llamar al método **Encrypt** con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".</span><span class="sxs-lookup"><span data-stu-id="5e86c-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="5e86c-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="5e86c-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="5e86c-138">Realizar la operación solicitada sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="5e86c-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="5e86c-139">La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido.</span><span class="sxs-lookup"><span data-stu-id="5e86c-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="5e86c-140">Esta marca solo se admite con el método **Encrypt** .</span><span class="sxs-lookup"><span data-stu-id="5e86c-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="5e86c-141">Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso.</span><span class="sxs-lookup"><span data-stu-id="5e86c-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="5e86c-142">Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="5e86c-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e86c-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e86c-143">Return value</span></span>

<span data-ttu-id="5e86c-144">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86c-144">Type: **uint32**</span></span>

<span data-ttu-id="5e86c-145">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5e86c-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="5e86c-146">Este método vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5e86c-146">This method returns immediately.</span></span> <span data-ttu-id="5e86c-147">Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="5e86c-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e86c-148">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e86c-148">Return code/value</span></span></th>
<th><span data-ttu-id="5e86c-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e86c-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="5e86c-150"><dt><strong>S_OK</strong></dt> <dt>0 (0X0)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-151">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e86c-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5e86c-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-153">Se proporciona el parámetro <em>EncryptionMethod</em> , pero no está dentro del intervalo conocido o no coincide con el valor de directiva de grupo actual.</span><span class="sxs-lookup"><span data-stu-id="5e86c-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5e86c-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-155">No existe ninguna clave de cifrado para el volumen.</span><span class="sxs-lookup"><span data-stu-id="5e86c-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="5e86c-156">Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar los protectores de clave para el volumen:</span><span class="sxs-lookup"><span data-stu-id="5e86c-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="5e86c-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="5e86c-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="5e86c-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="5e86c-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="5e86c-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="5e86c-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e86c-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="5e86c-163">
<strong>Windows Vista:</strong> Cuando no existe ninguna clave de cifrado para el volumen, se devuelve ERROR_INVALID_OPERATION en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5e86c-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="5e86c-164">El valor decimal es 4317 y el valor hexadecimal es 0x10DD.</span><span class="sxs-lookup"><span data-stu-id="5e86c-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5e86c-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-166">El método de cifrado proporcionado no coincide con el del volumen totalmente cifrado o parcial.</span><span class="sxs-lookup"><span data-stu-id="5e86c-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="5e86c-167">Para continuar con el cifrado, deje en blanco el parámetro <em>EncryptionMethod</em> o use un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="5e86c-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5e86c-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-169">No se puede cifrar el volumen porque este equipo está configurado para formar parte de un clúster de servidores.</span><span class="sxs-lookup"><span data-stu-id="5e86c-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5e86c-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-171">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5e86c-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="5e86c-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="5e86c-173">No se especifica ningún protector de clave de la &quot; contraseña numérica de tipo &quot; .</span><span class="sxs-lookup"><span data-stu-id="5e86c-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="5e86c-174">El directiva de grupo requiere una copia de seguridad de la información de recuperación en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5e86c-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="5e86c-175">Para agregar al menos un protector de clave de ese tipo, utilice el método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5e86c-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5e86c-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e86c-176">Remarks</span></span>

<span data-ttu-id="5e86c-177">Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión de modo completo para mantener el comportamiento compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e86c-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="5e86c-178">De este modo, la expectativa de seguridad de las aplicaciones y los scripts existentes no se interrumpirá con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5e86c-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="5e86c-179">Puede llamar a [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) para determinar si el cifrado está en curso y el porcentaje del volumen que se ha cifrado.</span><span class="sxs-lookup"><span data-stu-id="5e86c-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="5e86c-180">Una vez que el volumen está totalmente cifrado y se han agregado y habilitado protectores de clave, el estado de protección del volumen cambia a "activado".</span><span class="sxs-lookup"><span data-stu-id="5e86c-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="5e86c-181">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5e86c-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5e86c-182">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5e86c-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5e86c-183">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5e86c-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5e86c-184">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5e86c-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e86c-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e86c-185">Requirements</span></span>



| <span data-ttu-id="5e86c-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e86c-186">Requirement</span></span> | <span data-ttu-id="5e86c-187">Value</span><span class="sxs-lookup"><span data-stu-id="5e86c-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e86c-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e86c-188">Minimum supported client</span></span><br/> | <span data-ttu-id="5e86c-189">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e86c-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5e86c-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e86c-190">Minimum supported server</span></span><br/> | <span data-ttu-id="5e86c-191">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e86c-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e86c-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e86c-192">Namespace</span></span><br/>                | <span data-ttu-id="5e86c-193">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="5e86c-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5e86c-194">MOF</span><span class="sxs-lookup"><span data-stu-id="5e86c-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e86c-195"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e86c-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e86c-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e86c-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e86c-197">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="5e86c-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
