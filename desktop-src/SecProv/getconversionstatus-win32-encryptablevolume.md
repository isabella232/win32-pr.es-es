---
description: Indica el estado del cifrado o descifrado en el volumen.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907811"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8d27b-103">Método GetConversionStatus de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="8d27b-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8d27b-104">El método **GetConversionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el estado del cifrado o descifrado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="8d27b-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d27b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d27b-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="8d27b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d27b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d27b-107">*ConversionStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-108">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-109">Estado de cifrado o descifrado de volumen.</span><span class="sxs-lookup"><span data-stu-id="8d27b-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="8d27b-110">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8d27b-110">This can be one of the following values.</span></span>



| <span data-ttu-id="8d27b-111">Value</span><span class="sxs-lookup"><span data-stu-id="8d27b-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="8d27b-112">Significado</span><span class="sxs-lookup"><span data-stu-id="8d27b-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="8d27b-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="8d27b-114">En el caso de una unidad de disco duro estándar (HDD), el volumen se descifra por completo.</span><span class="sxs-lookup"><span data-stu-id="8d27b-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="8d27b-115">En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen se desbloquea de forma perpetua.</span><span class="sxs-lookup"><span data-stu-id="8d27b-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="8d27b-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="8d27b-117">En el caso de una unidad de disco duro estándar (HDD), el volumen está totalmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="8d27b-118">En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen no se desbloquea de forma perpetua.</span><span class="sxs-lookup"><span data-stu-id="8d27b-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="8d27b-119"><dt>**Durante**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="8d27b-120">El volumen está parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="8d27b-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="8d27b-122">El volumen está parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="8d27b-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="8d27b-124">El volumen se ha pausado durante el progreso del cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="8d27b-125">El volumen está parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="8d27b-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="8d27b-127">El volumen se ha pausado durante el progreso del descifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="8d27b-128">El volumen está parcialmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="8d27b-129">*EncryptionPercentage* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-130">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-131">Porcentaje del volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="8d27b-132">Es un entero comprendido entre 0 y 100, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="8d27b-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="8d27b-133">Debido al redondeo de números, un porcentaje de cifrado de 0 o 100 no indica necesariamente que el disco se haya descifrado o totalmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="8d27b-134">Use siempre *ConversionStatus* para determinar si el disco se ha descifrado completamente o está totalmente cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="8d27b-135">*EncryptionFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-136">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-136">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-137">Marcas que describen el comportamiento de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="8d27b-138">Combinación de 32 bits con los siguientes bits definidos actualmente.</span><span class="sxs-lookup"><span data-stu-id="8d27b-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="8d27b-139">Value</span><span class="sxs-lookup"><span data-stu-id="8d27b-139">Value</span></span>                                                                                  | <span data-ttu-id="8d27b-140">Significado</span><span class="sxs-lookup"><span data-stu-id="8d27b-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d27b-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="8d27b-142">Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="8d27b-143">Si el cifrado se ha pausado o detenido, la llamada al método de [**cifrado**](encrypt-win32-encryptablevolume.md) reanuda de forma eficaz la conversión y se omite el valor de este bit.</span><span class="sxs-lookup"><span data-stu-id="8d27b-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="8d27b-144">Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="8d27b-145">Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.</span><span class="sxs-lookup"><span data-stu-id="8d27b-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="8d27b-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="8d27b-147">Realice un borrado a petición del espacio libre del volumen.</span><span class="sxs-lookup"><span data-stu-id="8d27b-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="8d27b-148">Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".</span><span class="sxs-lookup"><span data-stu-id="8d27b-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="8d27b-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="8d27b-150">Realizar la operación solicitada sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="8d27b-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="8d27b-151">La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido.</span><span class="sxs-lookup"><span data-stu-id="8d27b-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="8d27b-152">Esta marca solo se admite con el método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="8d27b-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="8d27b-153">Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso.</span><span class="sxs-lookup"><span data-stu-id="8d27b-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="8d27b-154">Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="8d27b-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="8d27b-155">*WipingStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-156">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-156">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-157">Estado de limpieza de espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="8d27b-157">Free space wiping status.</span></span> <span data-ttu-id="8d27b-158">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8d27b-158">This can be one of the following values.</span></span>



| <span data-ttu-id="8d27b-159">Value</span><span class="sxs-lookup"><span data-stu-id="8d27b-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="8d27b-160">Significado</span><span class="sxs-lookup"><span data-stu-id="8d27b-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="8d27b-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="8d27b-162">No se ha borrado el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="8d27b-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="8d27b-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="8d27b-164">Se ha borrado el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="8d27b-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="8d27b-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="8d27b-166">La eliminación de espacio disponible está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="8d27b-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="8d27b-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="8d27b-168">Se pausó el barrido de espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="8d27b-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="8d27b-169">*WipingPercentage* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-170">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-170">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-171">Un valor de 0 a 100 que especifica el porcentaje de espacio libre que se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="8d27b-172">*PrecisionFactor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27b-173">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-173">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-174">Un valor de 0 a 4 que especifica el nivel de precisión</span><span class="sxs-lookup"><span data-stu-id="8d27b-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d27b-175">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d27b-175">Return value</span></span>

<span data-ttu-id="8d27b-176">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d27b-176">Type: **uint32**</span></span>

<span data-ttu-id="8d27b-177">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8d27b-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8d27b-178">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d27b-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="8d27b-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d27b-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8d27b-180"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="8d27b-181">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8d27b-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="8d27b-182"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="8d27b-183">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8d27b-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="8d27b-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d27b-184">Remarks</span></span>

<span data-ttu-id="8d27b-185">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8d27b-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d27b-186">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d27b-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8d27b-187">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8d27b-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d27b-188">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8d27b-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d27b-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d27b-189">Requirements</span></span>



| <span data-ttu-id="8d27b-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d27b-190">Requirement</span></span> | <span data-ttu-id="8d27b-191">Value</span><span class="sxs-lookup"><span data-stu-id="8d27b-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d27b-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d27b-192">Minimum supported client</span></span><br/> | <span data-ttu-id="8d27b-193">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d27b-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d27b-194">Minimum supported server</span></span><br/> | <span data-ttu-id="8d27b-195">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d27b-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d27b-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8d27b-196">Namespace</span></span><br/>                | <span data-ttu-id="8d27b-197">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="8d27b-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8d27b-198">MOF</span><span class="sxs-lookup"><span data-stu-id="8d27b-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d27b-199"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d27b-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d27b-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d27b-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d27b-201">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="8d27b-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
