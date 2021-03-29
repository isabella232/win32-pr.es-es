---
description: Usa la huella digital de certificado proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Método UnlockWithCertificateThumbprint de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809271"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1112e-103">Método UnlockWithCertificateThumbprint de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="1112e-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1112e-104">El método **UnlockWithCertificateThumbprint** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la huella digital de [*certificado*](../secgloss/c-gly.md) proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="1112e-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="1112e-105">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="1112e-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1112e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1112e-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="1112e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1112e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1112e-108">*CertThumbprint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1112e-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1112e-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="1112e-109">Type: **string**</span></span>

<span data-ttu-id="1112e-110">Se acepta un valor de huella digital de 0 y se produce una búsqueda del certificado adecuado en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="1112e-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="1112e-111">Si se encuentra un solo certificado de BitLocker, la búsqueda se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="1112e-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="1112e-112">Si no se encuentra ninguno o más de un certificado, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="1112e-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="1112e-113">*Código PIN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1112e-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1112e-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="1112e-114">Type: **string**</span></span>

<span data-ttu-id="1112e-115">Cadena de identificación personal especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1112e-115">A user-specified personal identification string.</span></span> <span data-ttu-id="1112e-116">Esta cadena debe estar formada por una secuencia de 4 a 20 dígitos.</span><span class="sxs-lookup"><span data-stu-id="1112e-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="1112e-117">Esta cadena se usa para autenticar de forma silenciosa el [*proveedor de almacenamiento de claves*](../secgloss/k-gly.md) (KSP) cuando se usa con una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1112e-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1112e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1112e-118">Return value</span></span>

<span data-ttu-id="1112e-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1112e-119">Type: **uint32**</span></span>

<span data-ttu-id="1112e-120">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1112e-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1112e-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1112e-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="1112e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1112e-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1112e-123"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="1112e-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1112e-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="1112e-125"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="1112e-126">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="1112e-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1112e-127">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1112e-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="1112e-128"><dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="1112e-129">No se puede desbloquear el volumen con la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="1112e-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="1112e-130"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="1112e-131">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="1112e-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="1112e-132">Debe especificar otro protector de clave.</span><span class="sxs-lookup"><span data-stu-id="1112e-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="1112e-133"><dt>**FVE \_ Error de E \_ PRIVATEKEY \_ auth \_**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="1112e-134">No se pudo autorizar la [*clave privada*](../secgloss/p-gly.md) asociada al certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="1112e-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="1112e-135">No se proporcionó la autorización de clave privada o la autorización proporcionada no era válida.</span><span class="sxs-lookup"><span data-stu-id="1112e-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1112e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1112e-136">Requirements</span></span>



| <span data-ttu-id="1112e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1112e-137">Requirement</span></span> | <span data-ttu-id="1112e-138">Value</span><span class="sxs-lookup"><span data-stu-id="1112e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1112e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1112e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1112e-140">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="1112e-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1112e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1112e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1112e-142">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1112e-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1112e-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1112e-143">Namespace</span></span><br/>                | <span data-ttu-id="1112e-144">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="1112e-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1112e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="1112e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1112e-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1112e-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1112e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1112e-148">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1112e-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
