---
description: Recupera la clave pública y la huella digital del certificado para un protector de clave pública.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Método GetKeyProtectorCertificate de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688157"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a6480-103">Método GetKeyProtectorCertificate de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="a6480-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a6480-104">El método **GetKeyProtectorCertificate** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la [*clave pública*](../secgloss/p-gly.md) y la huella digital del [*certificado*](../secgloss/c-gly.md) para un protector de clave pública.</span><span class="sxs-lookup"><span data-stu-id="a6480-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6480-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6480-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="a6480-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6480-107">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6480-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6480-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a6480-108">Type: **string**</span></span>

<span data-ttu-id="a6480-109">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="a6480-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="a6480-110">*PublicKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6480-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6480-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a6480-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="a6480-112">Matriz de bytes que especifica la clave pública.</span><span class="sxs-lookup"><span data-stu-id="a6480-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="a6480-113">*CertThumbprint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6480-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6480-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a6480-114">Type: **string**</span></span>

<span data-ttu-id="a6480-115">Cadena que especifica la huella digital del certificado.</span><span class="sxs-lookup"><span data-stu-id="a6480-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="a6480-116">*CertType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6480-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6480-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6480-117">Type: **uint32**</span></span>

<span data-ttu-id="a6480-118">Entero sin signo que especifica el tipo del protector de clave.</span><span class="sxs-lookup"><span data-stu-id="a6480-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="a6480-119">Este entero se usa para diferenciar entre el agente de recuperación de datos (DRA) y los certificados de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6480-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="a6480-120">Value</span><span class="sxs-lookup"><span data-stu-id="a6480-120">Value</span></span>                                                                        | <span data-ttu-id="a6480-121">Significado</span><span class="sxs-lookup"><span data-stu-id="a6480-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="a6480-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a6480-123">El certificado es un DRA.</span><span class="sxs-lookup"><span data-stu-id="a6480-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="a6480-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a6480-125">El certificado no es un DRA.</span><span class="sxs-lookup"><span data-stu-id="a6480-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6480-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6480-126">Return value</span></span>

<span data-ttu-id="a6480-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6480-127">Type: **uint32**</span></span>

<span data-ttu-id="a6480-128">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a6480-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a6480-129">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6480-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="a6480-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6480-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6480-131"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="a6480-132">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6480-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="a6480-133"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="a6480-134">El protector de clave especificado no es un protector de clave.</span><span class="sxs-lookup"><span data-stu-id="a6480-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="a6480-135">Debe especificar otro protector de clave.</span><span class="sxs-lookup"><span data-stu-id="a6480-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="a6480-136"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="a6480-137">Esta unidad está bloqueada por Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a6480-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="a6480-138">Debe desbloquear este volumen en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="a6480-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="a6480-139"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="a6480-140">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="a6480-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="a6480-141">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a6480-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="a6480-142"><dt>**FVE \_ Certificado de usuario de directiva de E \_ \_ \_ \_ requerido**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="a6480-143">Directiva de grupo requiere el uso de un certificado de usuario, como una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="a6480-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="a6480-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6480-144">Remarks</span></span>

<span data-ttu-id="a6480-145">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a6480-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6480-146">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a6480-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a6480-147">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a6480-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6480-148">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a6480-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6480-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6480-149">Requirements</span></span>



| <span data-ttu-id="a6480-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6480-150">Requirement</span></span> | <span data-ttu-id="a6480-151">Value</span><span class="sxs-lookup"><span data-stu-id="a6480-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6480-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6480-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a6480-153">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6480-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6480-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6480-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a6480-155">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6480-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6480-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6480-156">Namespace</span></span><br/>                | <span data-ttu-id="a6480-157">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="a6480-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a6480-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a6480-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6480-159"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6480-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6480-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6480-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6480-161">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="a6480-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
