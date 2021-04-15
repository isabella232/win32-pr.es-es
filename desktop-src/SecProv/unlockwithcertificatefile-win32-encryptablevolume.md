---
description: Usa el archivo de certificado proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Método UnlockWithCertificateFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668472"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9654a-103">Método UnlockWithCertificateFile de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="9654a-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9654a-104">El método **UnlockWithCertificateFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa el archivo de [*certificado*](../secgloss/c-gly.md) proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="9654a-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="9654a-105">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="9654a-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9654a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9654a-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="9654a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9654a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9654a-108">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9654a-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9654a-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="9654a-109">Type: **string**</span></span>

<span data-ttu-id="9654a-110">Una cadena que especifica la ubicación y el nombre del archivo. cer que se usa para recuperar la huella digital del certificado.</span><span class="sxs-lookup"><span data-stu-id="9654a-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="9654a-111">Se debe exportar un certificado de [*cifrado*](../secgloss/e-gly.md) en formato. cer ([*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) binario codificado [*x. 509*](../secgloss/x-gly.md) o x. 509 codificado en base-64).</span><span class="sxs-lookup"><span data-stu-id="9654a-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="9654a-112">El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.</span><span class="sxs-lookup"><span data-stu-id="9654a-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="9654a-113">*Código PIN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9654a-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9654a-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="9654a-114">Type: **string**</span></span>

<span data-ttu-id="9654a-115">Cadena de identificación personal especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9654a-115">A user-specified personal identification string.</span></span> <span data-ttu-id="9654a-116">Esta cadena debe estar formada por una secuencia de 4 a 20 dígitos.</span><span class="sxs-lookup"><span data-stu-id="9654a-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="9654a-117">Esta cadena se usa para autenticar de forma silenciosa el [*proveedor de almacenamiento de claves*](../secgloss/k-gly.md) (KSP) cuando se usa con una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9654a-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9654a-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9654a-118">Return value</span></span>

<span data-ttu-id="9654a-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9654a-119">Type: **uint32**</span></span>

<span data-ttu-id="9654a-120">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9654a-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9654a-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9654a-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9654a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9654a-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9654a-123"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="9654a-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9654a-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9654a-125"><dt>**Error \_ de \_No \_ se encontró el archivo**</dt> <dt>0000000002 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="9654a-126">El sistema no puede archivar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9654a-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9654a-127"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="9654a-128">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="9654a-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9654a-129">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9654a-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="9654a-130"><dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="9654a-131">No se puede desbloquear el volumen con la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="9654a-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="9654a-132"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="9654a-133">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="9654a-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="9654a-134">Debe especificar otro protector de clave.</span><span class="sxs-lookup"><span data-stu-id="9654a-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="9654a-135"><dt>**FVE \_ Error de E \_ PRIVATEKEY \_ auth \_**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="9654a-136">No se pudo autorizar la [*clave privada*](../secgloss/p-gly.md)asociada con el certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="9654a-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="9654a-137">No se proporcionó la autorización de la clave privada o la autorización proporcionada no era válida.</span><span class="sxs-lookup"><span data-stu-id="9654a-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9654a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9654a-138">Requirements</span></span>



| <span data-ttu-id="9654a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9654a-139">Requirement</span></span> | <span data-ttu-id="9654a-140">Value</span><span class="sxs-lookup"><span data-stu-id="9654a-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9654a-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9654a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9654a-142">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="9654a-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9654a-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9654a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9654a-144">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9654a-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9654a-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9654a-145">Namespace</span></span><br/>                | <span data-ttu-id="9654a-146">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="9654a-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9654a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9654a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9654a-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9654a-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9654a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9654a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9654a-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="9654a-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
