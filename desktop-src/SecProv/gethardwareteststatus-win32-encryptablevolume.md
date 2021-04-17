---
description: Proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Método GetHardwareTestStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688161"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="32dcf-103">Método GetHardwareTestStatus de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="32dcf-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="32dcf-104">El método **GetHardwareTestStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.</span><span class="sxs-lookup"><span data-stu-id="32dcf-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="32dcf-105">Use este método para mostrar si hay una prueba de hardware pendiente, así como el éxito o el fracaso de una prueba de hardware completada en el último reinicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="32dcf-106">Para solicitar una prueba de hardware, use el método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="32dcf-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32dcf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32dcf-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="32dcf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32dcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32dcf-109">*TestStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32dcf-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32dcf-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32dcf-110">Type: **uint32**</span></span>

<span data-ttu-id="32dcf-111">Especifica si hay una prueba de hardware pendiente, así como el éxito del error de una prueba de hardware completada en el último reinicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32dcf-112">Value</span><span class="sxs-lookup"><span data-stu-id="32dcf-112">Value</span></span></th>
<th><span data-ttu-id="32dcf-113">Significado</span><span class="sxs-lookup"><span data-stu-id="32dcf-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="32dcf-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="32dcf-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="32dcf-115">Si se solicitó una prueba, la prueba se realizó correctamente en el último reinicio del equipo y el cifrado del volumen ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="32dcf-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="32dcf-116">Para obtener el estado de cifrado, consulte el método <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="32dcf-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="32dcf-117">De lo contrario, no se ejecutó ninguna prueba en el último reinicio del equipo y no hay ninguna pendiente.</span><span class="sxs-lookup"><span data-stu-id="32dcf-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="32dcf-118"><dt><strong>Error</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="32dcf-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="32dcf-119">No se inició el cifrado de volumen.</span><span class="sxs-lookup"><span data-stu-id="32dcf-119">Volume encryption did not start.</span></span> <span data-ttu-id="32dcf-120">Se quitaron todos los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="32dcf-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="32dcf-121">Para resolver una prueba con errores:</span><span class="sxs-lookup"><span data-stu-id="32dcf-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="32dcf-122">Consulte la información del parámetro <em>TestError</em> .</span><span class="sxs-lookup"><span data-stu-id="32dcf-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="32dcf-123">Agregue protectores de clave y vuelva a usar el método <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="32dcf-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="32dcf-124"><dt><strong>Pendiente</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="32dcf-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="32dcf-125">Se ha solicitado una prueba que se ejecutará en el próximo reinicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="32dcf-126">*TestError* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32dcf-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32dcf-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32dcf-127">Type: **uint32**</span></span>

<span data-ttu-id="32dcf-128">Especifica el error de la última prueba de hardware completada.</span><span class="sxs-lookup"><span data-stu-id="32dcf-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="32dcf-129">Value</span><span class="sxs-lookup"><span data-stu-id="32dcf-129">Value</span></span>                                                                                               | <span data-ttu-id="32dcf-130">Significado</span><span class="sxs-lookup"><span data-stu-id="32dcf-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32dcf-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="32dcf-132">No se ha producido ningún error o no se ejecutó ninguna prueba de hardware en el último reinicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="32dcf-133"><dt> 2150694972 (0x8031003C)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="32dcf-134">\_ \_ \_ no \_ se encontró FVE E keyfile</span><span class="sxs-lookup"><span data-stu-id="32dcf-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="32dcf-135">No se encontró una unidad flash USB con un archivo de clave externa.</span><span class="sxs-lookup"><span data-stu-id="32dcf-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="32dcf-136">Si el error persiste, el equipo no podrá leer las unidades USB durante el reinicio.</span><span class="sxs-lookup"><span data-stu-id="32dcf-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="32dcf-137">Es posible que no pueda usar claves externas para desbloquear el volumen del sistema operativo durante el reinicio.</span><span class="sxs-lookup"><span data-stu-id="32dcf-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="32dcf-138"><dt> 2150694973 (0x8031003D)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="32dcf-139">FVE \_ E \_ keyfile \_ no válido</span><span class="sxs-lookup"><span data-stu-id="32dcf-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="32dcf-140">El archivo de clave externa en la unidad flash USB estaba dañado.</span><span class="sxs-lookup"><span data-stu-id="32dcf-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="32dcf-141">Pruebe una unidad flash USB diferente para almacenar el archivo de clave externa.</span><span class="sxs-lookup"><span data-stu-id="32dcf-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="32dcf-142"><dt> 2150694975 (0x8031003F)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="32dcf-143">FVE \_ E \_ TPM \_ deshabilitado</span><span class="sxs-lookup"><span data-stu-id="32dcf-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="32dcf-144">El TPM está deshabilitado o desactivado, o bien deshabilitado y desactivado.</span><span class="sxs-lookup"><span data-stu-id="32dcf-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="32dcf-145">Para activar el TPM, use el proveedor [**WMI \_ TPM de Win32**](win32-tpm.md) o ejecute el complemento Administración de TPM (TPM. msc).</span><span class="sxs-lookup"><span data-stu-id="32dcf-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="32dcf-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="32dcf-147">\_ \_ \_ PCR no válido de FVE E TPM \_</span><span class="sxs-lookup"><span data-stu-id="32dcf-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="32dcf-148">El TPM detectó un cambio en los servicios de reinicio del sistema operativo en el perfil de validación de plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="32dcf-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="32dcf-149">Quite cualquier CD o DVD de inicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="32dcf-150">Si el error persiste, compruebe que las actualizaciones de firmware y BIOS más recientes están instaladas y que el TPM está funcionando correctamente.</span><span class="sxs-lookup"><span data-stu-id="32dcf-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="32dcf-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="32dcf-152">FVE \_ E \_ PIN \_ no válido</span><span class="sxs-lookup"><span data-stu-id="32dcf-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="32dcf-153">El PIN proporcionado era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="32dcf-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32dcf-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32dcf-154">Return value</span></span>

<span data-ttu-id="32dcf-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32dcf-155">Type: **uint32**</span></span>

<span data-ttu-id="32dcf-156">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="32dcf-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="32dcf-157">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32dcf-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="32dcf-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="32dcf-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="32dcf-159"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="32dcf-160">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="32dcf-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="32dcf-161"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="32dcf-162">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="32dcf-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32dcf-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32dcf-163">Remarks</span></span>

<span data-ttu-id="32dcf-164">Para solicitar una prueba de hardware, use el método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="32dcf-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="32dcf-165">Para ejecutar una prueba de hardware cuando su estado es pendiente, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="32dcf-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="32dcf-166">Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa.</span><span class="sxs-lookup"><span data-stu-id="32dcf-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="32dcf-167">Este paso solo se aplica si el volumen tiene un protector de clave de tipo "clave externa" o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="32dcf-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="32dcf-168">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-168">Restart the computer.</span></span> <span data-ttu-id="32dcf-169">En el reinicio del equipo, la prueba de hardware se ejecuta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="32dcf-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="32dcf-170">Para cancelar la prueba de hardware, use el método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="32dcf-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="32dcf-171">Una prueba correcta determina que:</span><span class="sxs-lookup"><span data-stu-id="32dcf-171">A successful test determines that:</span></span>

-   <span data-ttu-id="32dcf-172">El TPM puede desbloquear el volumen si existe un protector de clave relacionado con TPM.</span><span class="sxs-lookup"><span data-stu-id="32dcf-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="32dcf-173">El equipo puede leer una unidad flash USB que contenga un archivo de clave externa durante el inicio si el volumen se puede desbloquear mediante una clave externa (incluida una clave de inicio).</span><span class="sxs-lookup"><span data-stu-id="32dcf-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="32dcf-174">Los resultados de la prueba de hardware no estarán disponibles después de realizar cambios en la conversión o después del siguiente reinicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="32dcf-175">Compruebe el registro de eventos del sistema para obtener información acerca de las pruebas de hardware que se ejecutaron previamente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="32dcf-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="32dcf-176">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="32dcf-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="32dcf-177">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="32dcf-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="32dcf-178">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="32dcf-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="32dcf-179">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="32dcf-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32dcf-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32dcf-180">Requirements</span></span>



| <span data-ttu-id="32dcf-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="32dcf-181">Requirement</span></span> | <span data-ttu-id="32dcf-182">Value</span><span class="sxs-lookup"><span data-stu-id="32dcf-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32dcf-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32dcf-183">Minimum supported client</span></span><br/> | <span data-ttu-id="32dcf-184">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="32dcf-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="32dcf-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32dcf-185">Minimum supported server</span></span><br/> | <span data-ttu-id="32dcf-186">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="32dcf-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32dcf-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32dcf-187">Namespace</span></span><br/>                | <span data-ttu-id="32dcf-188">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="32dcf-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="32dcf-189">MOF</span><span class="sxs-lookup"><span data-stu-id="32dcf-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32dcf-190"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32dcf-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32dcf-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="32dcf-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32dcf-192">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="32dcf-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
