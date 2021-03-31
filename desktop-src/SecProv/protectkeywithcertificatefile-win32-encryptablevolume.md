---
description: Valida el identificador de objeto (OID) de uso mejorado de clave (EKU) del certificado proporcionado.
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Método ProtectKeyWithCertificateFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 86d9557506dc9ff3c465bcb956391b3e4cf33791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907806"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="70a41-103">Método ProtectKeyWithCertificateFile de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="70a41-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="70a41-104">El método **ProtectKeyWithCertificateFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) valida el [*identificador de objeto*](../secgloss/o-gly.md) (OID) de uso mejorado de clave (EKU) del certificado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="70a41-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70a41-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="70a41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70a41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a41-107">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70a41-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70a41-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="70a41-108">Type: **string**</span></span>

<span data-ttu-id="70a41-109">Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="70a41-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="70a41-110">Si no se especifica este parámetro, el parámetro *FriendlyName* se crea con el nombre de sujeto del certificado.</span><span class="sxs-lookup"><span data-stu-id="70a41-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="70a41-111">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70a41-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a41-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="70a41-112">Type: **string**</span></span>

<span data-ttu-id="70a41-113">Cadena que especifica la ubicación y el nombre del archivo. cer que se usa para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70a41-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="70a41-114">Se debe exportar un certificado de cifrado en formato. cer ([*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) binario codificado [*x. 509*](../secgloss/x-gly.md) o x. 509 codificado en base-64).</span><span class="sxs-lookup"><span data-stu-id="70a41-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="70a41-115">El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.</span><span class="sxs-lookup"><span data-stu-id="70a41-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="70a41-116">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="70a41-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70a41-117">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="70a41-117">Type: **string**</span></span>

<span data-ttu-id="70a41-118">Una cadena que identifica de forma única el protector de clave creado que se puede usar para administrar este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="70a41-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="70a41-119">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="70a41-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a41-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70a41-120">Return value</span></span>

<span data-ttu-id="70a41-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a41-121">Type: **uint32**</span></span>

<span data-ttu-id="70a41-122">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="70a41-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="70a41-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70a41-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="70a41-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a41-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70a41-125"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="70a41-126">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="70a41-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="70a41-127"><dt>**FVE \_ E \_ no \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="70a41-128">El atributo EKU del certificado especificado no permite su uso para Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70a41-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="70a41-129">BitLocker no requiere que un certificado tenga un atributo EKU, pero si se configura uno, debe establecerse en un OID que coincida con el OID configurado para BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70a41-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="70a41-130"><dt>**FVE \_ Certificado de usuario de directiva de E \_ \_ \_ \_ no \_ permitido**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="70a41-131">Directiva de grupo no permite el uso de certificados de usuario, como tarjetas inteligentes, con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70a41-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="70a41-132"><dt>**FVE \_ El \_ certificado de usuario de directiva de E \_ \_ \_ debe \_ ser \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="70a41-133">Directiva de grupo requiere que proporcione una tarjeta inteligente para usar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70a41-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="70a41-134"><dt>**FVE \_ La \_ Directiva E \_ prohíbe \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="70a41-135">Directiva de grupo no permite el uso de certificados autofirmados.</span><span class="sxs-lookup"><span data-stu-id="70a41-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="70a41-136"><dt>**Error \_ de \_No \_ se encontró el archivo**</dt> <dt>0000000002 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="70a41-137">El sistema no encuentra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="70a41-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="70a41-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70a41-138">Remarks</span></span>

<span data-ttu-id="70a41-139">Si el OID no coincide con el que está asociado con el controlador de servicio en el registro, este método produce un error.</span><span class="sxs-lookup"><span data-stu-id="70a41-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="70a41-140">Esto impide que el usuario configure los protectores del agente de recuperación de datos (DRA) manualmente en el volumen.</span><span class="sxs-lookup"><span data-stu-id="70a41-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="70a41-141">Los Dra solo los establece el servicio.</span><span class="sxs-lookup"><span data-stu-id="70a41-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a41-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a41-142">Requirements</span></span>



| <span data-ttu-id="70a41-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a41-143">Requirement</span></span> | <span data-ttu-id="70a41-144">Value</span><span class="sxs-lookup"><span data-stu-id="70a41-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a41-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a41-145">Minimum supported client</span></span><br/> | <span data-ttu-id="70a41-146">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="70a41-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70a41-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a41-147">Minimum supported server</span></span><br/> | <span data-ttu-id="70a41-148">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="70a41-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70a41-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70a41-149">Namespace</span></span><br/>                | <span data-ttu-id="70a41-150">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="70a41-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="70a41-151">MOF</span><span class="sxs-lookup"><span data-stu-id="70a41-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a41-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a41-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a41-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="70a41-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a41-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="70a41-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
