---
description: Inicia el cifrado de un volumen del sistema operativo totalmente descifrado después de una prueba de hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Método EncryptAfterHardwareTest de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540942"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="91ed5-103">Método EncryptAfterHardwareTest de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="91ed5-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="91ed5-104">El método **EncryptAfterHardwareTest** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) inicia el cifrado de un volumen del sistema operativo totalmente descifrado después de una prueba de hardware.</span><span class="sxs-lookup"><span data-stu-id="91ed5-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="91ed5-105">Se requiere un reinicio para realizar esta prueba de hardware.</span><span class="sxs-lookup"><span data-stu-id="91ed5-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="91ed5-106">Utilice este método en lugar del método [**Encrypt**](encrypt-win32-encryptablevolume.md) para comprobar que BitLocker funcionará según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="91ed5-107">Si el disco duro está cifrado por hardware, este método no cifra los datos.</span><span class="sxs-lookup"><span data-stu-id="91ed5-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="91ed5-108">En su lugar, establece el estado de la banda en desbloqueado de "sin bloqueos".</span><span class="sxs-lookup"><span data-stu-id="91ed5-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="91ed5-109">Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.</span><span class="sxs-lookup"><span data-stu-id="91ed5-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91ed5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91ed5-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="91ed5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91ed5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ed5-112">*EncryptionMethod* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="91ed5-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="91ed5-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91ed5-113">Type: **uint32**</span></span>

<span data-ttu-id="91ed5-114">Especifica el algoritmo de cifrado y el tamaño de la clave que se usa para cifrar el volumen.</span><span class="sxs-lookup"><span data-stu-id="91ed5-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="91ed5-115">Deje este parámetro en blanco para usar el valor predeterminado de cero.</span><span class="sxs-lookup"><span data-stu-id="91ed5-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="91ed5-116">Si el volumen está cifrado parcial o totalmente, el valor de este parámetro debe ser 0 o coincidir con el método de cifrado existente del volumen.</span><span class="sxs-lookup"><span data-stu-id="91ed5-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="91ed5-117">Si se ha habilitado la configuración de directiva de grupo correspondiente con un valor válido, el valor de este parámetro debe ser 0 o coincidir con el valor directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="91ed5-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="91ed5-118">Si el valor de directiva de grupo correspondiente no es válido, se usa el valor predeterminado de AES 128 con difusor.</span><span class="sxs-lookup"><span data-stu-id="91ed5-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="91ed5-119">Value</span><span class="sxs-lookup"><span data-stu-id="91ed5-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="91ed5-120">Significado</span><span class="sxs-lookup"><span data-stu-id="91ed5-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="91ed5-121">No <dt>**especificado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="91ed5-122">Use el valor de directiva de grupo actual, si está disponible y es válido, o el método de cifrado predeterminado de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="91ed5-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="91ed5-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="91ed5-124">AES 128 CON DIFUSOR</span><span class="sxs-lookup"><span data-stu-id="91ed5-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="91ed5-125">Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y usando un tamaño de clave de AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="91ed5-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="91ed5-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="91ed5-127">AES 256 CON DIFUSOR</span><span class="sxs-lookup"><span data-stu-id="91ed5-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="91ed5-128">Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y usando un tamaño de clave de AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="91ed5-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="91ed5-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="91ed5-130">Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) y usando un tamaño de clave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="91ed5-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="91ed5-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="91ed5-132">Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) y usando un tamaño de clave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="91ed5-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="91ed5-133">*EncryptionFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="91ed5-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="91ed5-134">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91ed5-134">Type: **uint32**</span></span>

<span data-ttu-id="91ed5-135">Marcas que describen el comportamiento de cifrado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="91ed5-136">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise y Windows server 2008:** Este parámetro no está disponible.</span><span class="sxs-lookup"><span data-stu-id="91ed5-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="91ed5-137">Combinación de 32 bits con los siguientes bits definidos actualmente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="91ed5-138">Value</span><span class="sxs-lookup"><span data-stu-id="91ed5-138">Value</span></span>                                                                                  | <span data-ttu-id="91ed5-139">Significado</span><span class="sxs-lookup"><span data-stu-id="91ed5-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91ed5-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="91ed5-141">Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="91ed5-142">Si el cifrado se ha pausado o detenido, la llamada al método de [**cifrado**](encrypt-win32-encryptablevolume.md) reanuda de forma eficaz la conversión y se omite el valor de este bit.</span><span class="sxs-lookup"><span data-stu-id="91ed5-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="91ed5-143">Este bit solo tiene efecto cuando los métodos **Encrypt** o **EncryptAfterHardwareTest** inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="91ed5-144">Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.</span><span class="sxs-lookup"><span data-stu-id="91ed5-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="91ed5-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="91ed5-146">Realice un borrado a petición del espacio libre del volumen.</span><span class="sxs-lookup"><span data-stu-id="91ed5-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="91ed5-147">Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".</span><span class="sxs-lookup"><span data-stu-id="91ed5-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="91ed5-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="91ed5-149">Realizar la operación solicitada sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="91ed5-150">La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido.</span><span class="sxs-lookup"><span data-stu-id="91ed5-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="91ed5-151">Esta marca solo se admite con el método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="91ed5-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="91ed5-152">Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso.</span><span class="sxs-lookup"><span data-stu-id="91ed5-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="91ed5-153">Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="91ed5-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ed5-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91ed5-154">Return value</span></span>

<span data-ttu-id="91ed5-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91ed5-155">Type: **uint32**</span></span>

<span data-ttu-id="91ed5-156">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="91ed5-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="91ed5-157">Este método vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-157">This method returns immediately.</span></span> <span data-ttu-id="91ed5-158">Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="91ed5-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91ed5-159">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91ed5-159">Return code/value</span></span></th>
<th><span data-ttu-id="91ed5-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="91ed5-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="91ed5-161"><dt><strong>S_OK</strong></dt> <dt>0 (0X0)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-162">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="91ed5-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-164">Se proporciona el parámetro <em>EncryptionMethod</em> , pero no está dentro del intervalo conocido o no coincide con el valor de directiva de grupo actual.</span><span class="sxs-lookup"><span data-stu-id="91ed5-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="91ed5-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-166">No existe ninguna clave de cifrado para el volumen.</span><span class="sxs-lookup"><span data-stu-id="91ed5-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="91ed5-167">Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar los protectores de clave para el volumen:</span><span class="sxs-lookup"><span data-stu-id="91ed5-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="91ed5-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="91ed5-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-175">No se puede cifrar el volumen porque este equipo está configurado para formar parte de un clúster de servidores.</span><span class="sxs-lookup"><span data-stu-id="91ed5-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="91ed5-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-177">No se puede encontrar ningún protector de clave del tipo &quot; TPM &quot; , &quot; TPM y PIN &quot; , &quot; TPM, PIN y clave &quot; de inicio, &quot; TPM y clave de inicio, &quot; o clave &quot; externa &quot; .</span><span class="sxs-lookup"><span data-stu-id="91ed5-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="91ed5-178">La prueba de hardware solo implica los protectores de clave anteriores.</span><span class="sxs-lookup"><span data-stu-id="91ed5-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="91ed5-179">Si todavía desea ejecutar una prueba de hardware, debe usar uno de los métodos siguientes para especificar los protectores de clave para el volumen:</span><span class="sxs-lookup"><span data-stu-id="91ed5-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="91ed5-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="91ed5-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-187">El volumen se ha cifrado parcial o totalmente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="91ed5-188">La prueba de hardware se aplica antes de que se produzca el cifrado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="91ed5-189">Si todavía desea ejecutar la prueba, use primero el método <a href="decrypt-win32-encryptablevolume.md"><strong>descifrado</strong></a> y, a continuación, use uno de los métodos siguientes para agregar protectores de clave:</span><span class="sxs-lookup"><span data-stu-id="91ed5-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="91ed5-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="91ed5-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="91ed5-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="91ed5-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-196">El volumen es un volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="91ed5-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="91ed5-197">La prueba de hardware solo se aplica a los volúmenes que pueden iniciar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="91ed5-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="91ed5-198">Ejecute este método en el volumen del sistema operativo iniciado actualmente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="91ed5-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="91ed5-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="91ed5-200">No se especifica ningún protector de clave de la &quot; contraseña numérica de tipo &quot; .</span><span class="sxs-lookup"><span data-stu-id="91ed5-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="91ed5-201">El directiva de grupo requiere una copia de seguridad de la información de recuperación en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="91ed5-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="91ed5-202">Para agregar al menos un protector de clave de ese tipo, utilice el método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="91ed5-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="91ed5-203">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91ed5-203">Remarks</span></span>

<span data-ttu-id="91ed5-204">Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión de modo completo para mantener el comportamiento compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="91ed5-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="91ed5-205">De este modo, la expectativa de seguridad de las aplicaciones y los scripts existentes no se interrumpirá con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="91ed5-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="91ed5-206">A diferencia del método [**Encrypt**](encrypt-win32-encryptablevolume.md) , este método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="91ed5-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="91ed5-207">Comprueba si el TPM podrá desbloquear el volumen, si existe un protector de clave relacionado con TPM.</span><span class="sxs-lookup"><span data-stu-id="91ed5-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="91ed5-208">Comprueba si el equipo puede leer una unidad flash USB que contenga un archivo de clave externa durante el inicio, en caso de que el volumen se desbloquee con una clave externa (incluida una clave de inicio).</span><span class="sxs-lookup"><span data-stu-id="91ed5-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="91ed5-209">Requiere un reinicio del equipo para ejecutar la prueba de hardware.</span><span class="sxs-lookup"><span data-stu-id="91ed5-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="91ed5-210">Inicia el cifrado solo si la prueba de hardware se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="91ed5-211">No se puede usar en un volumen de datos, en un volumen parcial o totalmente cifrado, o para reanudar el cifrado.</span><span class="sxs-lookup"><span data-stu-id="91ed5-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="91ed5-212">Antes de ejecutar este método, use los métodos siguientes para crear los protectores de clave relacionados:</span><span class="sxs-lookup"><span data-stu-id="91ed5-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="91ed5-213">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="91ed5-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="91ed5-214">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="91ed5-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="91ed5-215">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="91ed5-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="91ed5-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="91ed5-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="91ed5-217">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="91ed5-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="91ed5-218">Después de ejecutar este método, siga estos pasos adicionales:</span><span class="sxs-lookup"><span data-stu-id="91ed5-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="91ed5-219">Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa.</span><span class="sxs-lookup"><span data-stu-id="91ed5-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="91ed5-220">Este paso solo se aplica si el volumen tiene un protector de clave de tipo "clave externa" o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="91ed5-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="91ed5-221">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="91ed5-221">Restart the computer.</span></span>

<span data-ttu-id="91ed5-222">En el reinicio del equipo, la prueba de hardware se ejecuta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="91ed5-223">El cifrado se inicia si la prueba de hardware se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="91ed5-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="91ed5-224">De lo contrario, intente resolver cualquier error de hardware.</span><span class="sxs-lookup"><span data-stu-id="91ed5-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="91ed5-225">Ejecute [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) después de reiniciar el equipo para obtener los resultados de las pruebas.</span><span class="sxs-lookup"><span data-stu-id="91ed5-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="91ed5-226">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="91ed5-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="91ed5-227">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="91ed5-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="91ed5-228">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="91ed5-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="91ed5-229">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="91ed5-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91ed5-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ed5-230">Requirements</span></span>



| <span data-ttu-id="91ed5-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ed5-231">Requirement</span></span> | <span data-ttu-id="91ed5-232">Value</span><span class="sxs-lookup"><span data-stu-id="91ed5-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ed5-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ed5-233">Minimum supported client</span></span><br/> | <span data-ttu-id="91ed5-234">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="91ed5-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="91ed5-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ed5-235">Minimum supported server</span></span><br/> | <span data-ttu-id="91ed5-236">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91ed5-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91ed5-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="91ed5-237">Namespace</span></span><br/>                | <span data-ttu-id="91ed5-238">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="91ed5-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="91ed5-239">MOF</span><span class="sxs-lookup"><span data-stu-id="91ed5-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91ed5-240"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ed5-241">Vea también</span><span class="sxs-lookup"><span data-stu-id="91ed5-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ed5-242">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="91ed5-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
