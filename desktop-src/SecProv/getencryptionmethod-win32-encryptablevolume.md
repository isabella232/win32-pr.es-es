---
description: Indica el algoritmo de cifrado y el tamaño de la clave usados en el volumen.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Método GetEncryptionMethod de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688168"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d78fb-103">Método GetEncryptionMethod de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d78fb-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d78fb-104">El método **GetEncryptionMethod** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el algoritmo de cifrado y el tamaño de clave usados en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d78fb-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="d78fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d78fb-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="d78fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d78fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78fb-107">*EncryptionMethod* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d78fb-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d78fb-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d78fb-108">Type: **uint32**</span></span>

<span data-ttu-id="d78fb-109">Entero sin signo que especifica el algoritmo de cifrado y el tamaño de clave usados en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d78fb-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="d78fb-110">Value</span><span class="sxs-lookup"><span data-stu-id="d78fb-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="d78fb-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d78fb-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="d78fb-112"><dt>**Ninguno**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="d78fb-113">El volumen no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="d78fb-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="d78fb-114"><dt>**AES \_ 128 \_ con \_ difusor**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d78fb-115">El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave de AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="d78fb-116">Este método ya no está disponible en los dispositivos que ejecutan Windows 8.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d78fb-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="d78fb-117"><dt>**AES \_ 256 \_ con \_ difusor**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="d78fb-118">El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave de AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="d78fb-119">Este método ya no está disponible en los dispositivos que ejecutan Windows 8.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d78fb-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="d78fb-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="d78fb-121">El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) con un tamaño de clave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="d78fb-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="d78fb-123">El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) con un tamaño de clave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="d78fb-124"><dt>**Hardware \_ de CIFRAdo**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="d78fb-125">El volumen se ha cifrado total o parcialmente con las capacidades de hardware de la unidad.</span><span class="sxs-lookup"><span data-stu-id="d78fb-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="d78fb-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="d78fb-127">El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave de AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="d78fb-128">Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d78fb-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="d78fb-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="d78fb-130">El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave de AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d78fb-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="d78fb-131">Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d78fb-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="d78fb-132"><dt>(UInt32) – 1</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="d78fb-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="d78fb-133">UNKNOWN</span></span><br/> <span data-ttu-id="d78fb-134">El volumen se ha cifrado total o parcialmente con un algoritmo y un tamaño de clave desconocidos.</span><span class="sxs-lookup"><span data-stu-id="d78fb-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d78fb-135">*SelfEncryptionDriveEncryptionMethod* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d78fb-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d78fb-136">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d78fb-136">Type: **string**</span></span>

<span data-ttu-id="d78fb-137">El algoritmo de cifrado se configura en la unidad de cifrado automático.</span><span class="sxs-lookup"><span data-stu-id="d78fb-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="d78fb-138">Una cadena nula significa que BitLocker usa el cifrado de software o no se indica ningún método de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d78fb-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78fb-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d78fb-139">Return value</span></span>

<span data-ttu-id="d78fb-140">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d78fb-140">Type: **uint32**</span></span>

<span data-ttu-id="d78fb-141">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d78fb-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d78fb-142">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d78fb-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d78fb-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78fb-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d78fb-144"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d78fb-145">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d78fb-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d78fb-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d78fb-146">Remarks</span></span>

<span data-ttu-id="d78fb-147">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d78fb-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d78fb-148">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d78fb-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d78fb-149">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d78fb-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d78fb-150">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d78fb-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d78fb-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d78fb-151">Requirements</span></span>



| <span data-ttu-id="d78fb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d78fb-152">Requirement</span></span> | <span data-ttu-id="d78fb-153">Value</span><span class="sxs-lookup"><span data-stu-id="d78fb-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d78fb-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d78fb-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d78fb-155">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d78fb-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d78fb-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d78fb-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d78fb-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d78fb-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d78fb-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d78fb-158">Namespace</span></span><br/>                | <span data-ttu-id="d78fb-159">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d78fb-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d78fb-160">MOF</span><span class="sxs-lookup"><span data-stu-id="d78fb-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d78fb-161"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d78fb-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d78fb-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="d78fb-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d78fb-163">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d78fb-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
