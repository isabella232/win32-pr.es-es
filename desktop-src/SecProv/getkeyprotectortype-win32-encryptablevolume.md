---
description: Indica el tipo de un protector de clave determinado.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Método GetKeyProtectorType de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546406"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="84037-103">Método GetKeyProtectorType de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="84037-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="84037-104">El método **GetKeyProtectorType** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el tipo de un protector de clave determinado.</span><span class="sxs-lookup"><span data-stu-id="84037-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="84037-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84037-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="84037-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84037-107">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84037-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84037-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="84037-108">Type: **string**</span></span>

<span data-ttu-id="84037-109">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="84037-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="84037-110">*KeyProtectorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84037-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84037-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84037-111">Type: **uint32**</span></span>

<span data-ttu-id="84037-112">Entero sin signo que especifica el tipo del protector de clave.</span><span class="sxs-lookup"><span data-stu-id="84037-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="84037-113">Value</span><span class="sxs-lookup"><span data-stu-id="84037-113">Value</span></span>                                                                         | <span data-ttu-id="84037-114">Significado</span><span class="sxs-lookup"><span data-stu-id="84037-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="84037-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84037-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="84037-116">Desconocido u otro tipo de protector</span><span class="sxs-lookup"><span data-stu-id="84037-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="84037-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="84037-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="84037-118">Módulo de plataforma segura (TPM)</span><span class="sxs-lookup"><span data-stu-id="84037-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="84037-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84037-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="84037-120">Clave externa</span><span class="sxs-lookup"><span data-stu-id="84037-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="84037-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="84037-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="84037-122">Contraseña numérica</span><span class="sxs-lookup"><span data-stu-id="84037-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="84037-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="84037-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="84037-124">TPM y PIN</span><span class="sxs-lookup"><span data-stu-id="84037-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="84037-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="84037-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="84037-126">TPM y clave de inicio</span><span class="sxs-lookup"><span data-stu-id="84037-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="84037-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="84037-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="84037-128">TPM y clave de inicio y PIN</span><span class="sxs-lookup"><span data-stu-id="84037-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="84037-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="84037-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="84037-130">Clave pública</span><span class="sxs-lookup"><span data-stu-id="84037-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="84037-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="84037-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="84037-132">Passphrase</span><span class="sxs-lookup"><span data-stu-id="84037-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="84037-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="84037-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="84037-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="84037-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="84037-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="84037-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="84037-136">Protector de CryptoAPI Next Generation (CNG)</span><span class="sxs-lookup"><span data-stu-id="84037-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84037-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84037-137">Return value</span></span>

<span data-ttu-id="84037-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84037-138">Type: **uint32**</span></span>

<span data-ttu-id="84037-139">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="84037-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="84037-140">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84037-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="84037-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="84037-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84037-142"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="84037-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="84037-143">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="84037-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="84037-144"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="84037-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="84037-145">El parámetro *VolumeKeyProtectorID* no hace referencia a un *KeyProtectorType* válido.</span><span class="sxs-lookup"><span data-stu-id="84037-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="84037-146"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="84037-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="84037-147">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="84037-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="84037-148">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84037-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="84037-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84037-149">Remarks</span></span>

<span data-ttu-id="84037-150">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="84037-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84037-151">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="84037-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="84037-152">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="84037-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84037-153">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="84037-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84037-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84037-154">Requirements</span></span>



| <span data-ttu-id="84037-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="84037-155">Requirement</span></span> | <span data-ttu-id="84037-156">Value</span><span class="sxs-lookup"><span data-stu-id="84037-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84037-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84037-157">Minimum supported client</span></span><br/> | <span data-ttu-id="84037-158">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="84037-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84037-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84037-159">Minimum supported server</span></span><br/> | <span data-ttu-id="84037-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="84037-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84037-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84037-161">Namespace</span></span><br/>                | <span data-ttu-id="84037-162">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="84037-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="84037-163">MOF</span><span class="sxs-lookup"><span data-stu-id="84037-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84037-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84037-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84037-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="84037-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84037-166">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="84037-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
