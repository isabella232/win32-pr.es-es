---
description: 'Método ProtectKeyWithCertificateThumbprint de la clase Win32_EncryptableVolume: valida el identificador de objeto (OID) uso mejorado de clave (EKU) del certificado proporcionado.'
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Método ProtectKeyWithCertificateThumbprint de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110583"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="51ff0-103">Método ProtectKeyWithCertificateThumbprint de la clase EncryptableVolume de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="51ff0-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="51ff0-104">El **método ProtectKeyWithCertificateThumbprint** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) valida el identificador de objeto (OID) uso mejorado de clave (EKU) del certificado proporcionado. [](../secgloss/o-gly.md)</span><span class="sxs-lookup"><span data-stu-id="51ff0-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ff0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51ff0-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="51ff0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51ff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ff0-107">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="51ff0-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51ff0-108">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51ff0-108">Type: **string**</span></span>

<span data-ttu-id="51ff0-109">Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="51ff0-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="51ff0-110">Si no se especifica este parámetro, el *parámetro FriendlyName* se crea mediante el nombre del sujeto en el certificado.</span><span class="sxs-lookup"><span data-stu-id="51ff0-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="51ff0-111">*CertThumbprint* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="51ff0-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ff0-112">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51ff0-112">Type: **string**</span></span>

<span data-ttu-id="51ff0-113">Cadena que especifica la huella digital del certificado.</span><span class="sxs-lookup"><span data-stu-id="51ff0-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="51ff0-114">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="51ff0-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51ff0-115">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51ff0-115">Type: **string**</span></span>

<span data-ttu-id="51ff0-116">Cadena que identifica de forma única el protector de clave creado que se puede usar para administrar este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="51ff0-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="51ff0-117">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.</span><span class="sxs-lookup"><span data-stu-id="51ff0-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ff0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51ff0-118">Return value</span></span>

<span data-ttu-id="51ff0-119">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="51ff0-119">Type: **uint32**</span></span>

<span data-ttu-id="51ff0-120">Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="51ff0-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="51ff0-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51ff0-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="51ff0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="51ff0-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51ff0-123"><dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="51ff0-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="51ff0-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="51ff0-125"><dt>**ERROR \_ DATOS \_ NO VÁLIDOS**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="51ff0-126">Los datos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="51ff0-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="51ff0-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="51ff0-128">El atributo EKU del certificado especificado no permite que se utilice para Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff0-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="51ff0-129">BitLocker no requiere que un certificado tenga un atributo EKU, pero si se configura uno, debe establecerse en un OID que coincida con el OID configurado para BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff0-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="51ff0-130"><dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT \_ \_ \_ \_ ALLOWED**</dt> <dt>2150695026 (0X80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="51ff0-131">directiva de grupo no permite que los certificados de usuario, como las tarjetas inteligentes, se utilicen con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff0-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="51ff0-132"><dt>**FVE \_ E \_ POLICY USER CERT DEBE SER \_ \_ \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="51ff0-133">directiva de grupo requiere que proporcione una tarjeta inteligente para usar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff0-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="51ff0-134"><dt>**FVE \_ E \_ POLICY PROHÍBE LA FIRMA \_ \_ PROPIA**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="51ff0-135">directiva de grupo no permite el uso de certificados autofirmados.</span><span class="sxs-lookup"><span data-stu-id="51ff0-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="51ff0-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51ff0-136">Remarks</span></span>

<span data-ttu-id="51ff0-137">Si el OID no coincide con el asociado al controlador de servicio en el Registro, se produce un error en este método.</span><span class="sxs-lookup"><span data-stu-id="51ff0-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="51ff0-138">Esto evita que el usuario ajuste los protectores del agente de recuperación de datos (DRA) manualmente en el volumen.</span><span class="sxs-lookup"><span data-stu-id="51ff0-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="51ff0-139">Los DRA solo los establecerá el servicio.</span><span class="sxs-lookup"><span data-stu-id="51ff0-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ff0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ff0-140">Requirements</span></span>



| <span data-ttu-id="51ff0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ff0-141">Requirement</span></span> | <span data-ttu-id="51ff0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="51ff0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ff0-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ff0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="51ff0-144">Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="51ff0-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51ff0-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ff0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="51ff0-146">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="51ff0-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="51ff0-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51ff0-147">Namespace</span></span><br/>                | <span data-ttu-id="51ff0-148">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="51ff0-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="51ff0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="51ff0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51ff0-150"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="51ff0-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ff0-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51ff0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ff0-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="51ff0-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
