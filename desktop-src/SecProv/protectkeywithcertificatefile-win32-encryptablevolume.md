---
description: 'Método ProtectKeyWithCertificateFile de la clase Win32_EncryptableVolume : valida el identificador de objeto (OID) uso mejorado de clave (EKU) del certificado proporcionado.'
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Método ProtectKeyWithCertificateFile de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110572"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="be7db-103">Método ProtectKeyWithCertificateFile de la clase EncryptableVolume de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="be7db-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="be7db-104">El **método ProtectKeyWithCertificateFile** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) valida el identificador de objeto (EKU) uso mejorado de clave (EKU) del certificado proporcionado. [](../secgloss/o-gly.md)</span><span class="sxs-lookup"><span data-stu-id="be7db-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be7db-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="be7db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be7db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7db-107">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="be7db-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be7db-108">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7db-108">Type: **string**</span></span>

<span data-ttu-id="be7db-109">Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="be7db-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="be7db-110">Si no se especifica este parámetro, el *parámetro FriendlyName* se crea mediante el nombre del sujeto en el certificado.</span><span class="sxs-lookup"><span data-stu-id="be7db-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="be7db-111">*FileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="be7db-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be7db-112">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7db-112">Type: **string**</span></span>

<span data-ttu-id="be7db-113">Cadena que especifica la ubicación y el nombre del archivo .cer usado para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="be7db-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="be7db-114">Un certificado de cifrado debe exportarse en formato .cer ([*reglas de codificación distinguida*](../secgloss/d-gly.md) (DER) binario codificado [*X.509*](../secgloss/x-gly.md) o X.509 codificado en Base-64).</span><span class="sxs-lookup"><span data-stu-id="be7db-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="be7db-115">El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.</span><span class="sxs-lookup"><span data-stu-id="be7db-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="be7db-116">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be7db-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be7db-117">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7db-117">Type: **string**</span></span>

<span data-ttu-id="be7db-118">Cadena que identifica de forma única el protector de clave creado que se puede usar para administrar este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="be7db-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="be7db-119">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.</span><span class="sxs-lookup"><span data-stu-id="be7db-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7db-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be7db-120">Return value</span></span>

<span data-ttu-id="be7db-121">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="be7db-121">Type: **uint32**</span></span>

<span data-ttu-id="be7db-122">Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="be7db-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="be7db-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be7db-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="be7db-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7db-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be7db-125"><dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="be7db-126">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="be7db-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="be7db-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="be7db-128">El atributo EKU del certificado especificado no permite que se utilice para Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="be7db-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="be7db-129">BitLocker no requiere que un certificado tenga un atributo EKU, pero si uno está configurado, debe establecerse en un OID que coincida con el OID configurado para BitLocker.</span><span class="sxs-lookup"><span data-stu-id="be7db-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="be7db-130"><dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT \_ \_ \_ \_ ALLOWED**</dt> <dt>2150695026 (0X80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="be7db-131">directiva de grupo no permite que los certificados de usuario, como las tarjetas inteligentes, se utilicen con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="be7db-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="be7db-132"><dt>**FVE \_ E \_ POLICY USER CERT DEBE SER \_ \_ \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="be7db-133">directiva de grupo requiere que proporcione una tarjeta inteligente para usar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="be7db-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="be7db-134"><dt>**FVE \_ E \_ POLICY PROHÍBE LA FIRMA \_ \_ PROPIA**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="be7db-135">directiva de grupo no permite el uso de certificados autofirmados.</span><span class="sxs-lookup"><span data-stu-id="be7db-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="be7db-136"><dt>**ERROR \_ ARCHIVO \_ NO \_ ENCONTRADO**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="be7db-137">El sistema no puede encontrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="be7db-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="be7db-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be7db-138">Remarks</span></span>

<span data-ttu-id="be7db-139">Si el OID no coincide con el asociado al controlador de servicio en el Registro, se produce un error en este método.</span><span class="sxs-lookup"><span data-stu-id="be7db-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="be7db-140">Esto evita que el usuario ajuste los protectores del agente de recuperación de datos (DRA) manualmente en el volumen.</span><span class="sxs-lookup"><span data-stu-id="be7db-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="be7db-141">Los DRA solo los establecerá el servicio.</span><span class="sxs-lookup"><span data-stu-id="be7db-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7db-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7db-142">Requirements</span></span>



| <span data-ttu-id="be7db-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7db-143">Requirement</span></span> | <span data-ttu-id="be7db-144">Valor</span><span class="sxs-lookup"><span data-stu-id="be7db-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7db-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7db-145">Minimum supported client</span></span><br/> | <span data-ttu-id="be7db-146">Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="be7db-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be7db-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7db-147">Minimum supported server</span></span><br/> | <span data-ttu-id="be7db-148">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="be7db-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be7db-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be7db-149">Namespace</span></span><br/>                | <span data-ttu-id="be7db-150">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="be7db-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="be7db-151">MOF</span><span class="sxs-lookup"><span data-stu-id="be7db-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be7db-152"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="be7db-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7db-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="be7db-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7db-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="be7db-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
