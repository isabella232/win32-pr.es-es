---
description: Indica si los protectores están disponibles para el volumen.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Método IsKeyProtectorAvailable de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275318"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="31eee-103">Método IsKeyProtectorAvailable de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="31eee-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="31eee-104">El método **IsKeyProtectorAvailable** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si los protectores están disponibles para el volumen.</span><span class="sxs-lookup"><span data-stu-id="31eee-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="31eee-105">Si se proporciona un tipo de protector, el método indica si los protectores del tipo especificado están disponibles para el volumen.</span><span class="sxs-lookup"><span data-stu-id="31eee-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="31eee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31eee-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="31eee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31eee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31eee-108">*KeyProtectorType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="31eee-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31eee-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31eee-109">Type: **uint32**</span></span>

<span data-ttu-id="31eee-110">Entero sin signo que indica el tipo de protector de clave de volumen consultado.</span><span class="sxs-lookup"><span data-stu-id="31eee-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="31eee-111">Si no se especifica este parámetro, se consultan todos los protectores de clave disponibles del volumen.</span><span class="sxs-lookup"><span data-stu-id="31eee-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="31eee-112">Value</span><span class="sxs-lookup"><span data-stu-id="31eee-112">Value</span></span>                                                                         | <span data-ttu-id="31eee-113">Significado</span><span class="sxs-lookup"><span data-stu-id="31eee-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="31eee-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="31eee-115">Todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="31eee-115">All types.</span></span><br/> <span data-ttu-id="31eee-116">Se consultan todos los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="31eee-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="31eee-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="31eee-118">Módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="31eee-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="31eee-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="31eee-120">Clave externa.</span><span class="sxs-lookup"><span data-stu-id="31eee-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="31eee-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="31eee-122">Contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="31eee-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="31eee-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="31eee-124">TPM y PIN.</span><span class="sxs-lookup"><span data-stu-id="31eee-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="31eee-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="31eee-126">TPM y clave de inicio.</span><span class="sxs-lookup"><span data-stu-id="31eee-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="31eee-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="31eee-128">TPM y clave de inicio y PIN.</span><span class="sxs-lookup"><span data-stu-id="31eee-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="31eee-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="31eee-130">Clave pública.</span><span class="sxs-lookup"><span data-stu-id="31eee-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="31eee-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="31eee-132">Frase.</span><span class="sxs-lookup"><span data-stu-id="31eee-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="31eee-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="31eee-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="31eee-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="31eee-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="31eee-136">Identificador de seguridad (SID)</span><span class="sxs-lookup"><span data-stu-id="31eee-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="31eee-137">*IsKeyProtectorAvailable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31eee-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31eee-138">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="31eee-138">Type: **boolean**</span></span>

<span data-ttu-id="31eee-139">Valor booleano que indica si existe un protector de clave de volumen del tipo especificado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="31eee-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31eee-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31eee-140">Return value</span></span>

<span data-ttu-id="31eee-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31eee-141">Type: **uint32**</span></span>

<span data-ttu-id="31eee-142">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="31eee-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="31eee-143">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31eee-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="31eee-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="31eee-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31eee-145"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="31eee-146">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="31eee-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="31eee-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="31eee-148">Se ha especificado el parámetro *KeyProtectorType* pero no hace referencia a un tipo de protector de clave válido.</span><span class="sxs-lookup"><span data-stu-id="31eee-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31eee-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31eee-149">Remarks</span></span>

<span data-ttu-id="31eee-150">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="31eee-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="31eee-151">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="31eee-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="31eee-152">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="31eee-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="31eee-153">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="31eee-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31eee-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31eee-154">Requirements</span></span>



| <span data-ttu-id="31eee-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="31eee-155">Requirement</span></span> | <span data-ttu-id="31eee-156">Value</span><span class="sxs-lookup"><span data-stu-id="31eee-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31eee-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31eee-157">Minimum supported client</span></span><br/> | <span data-ttu-id="31eee-158">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="31eee-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="31eee-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31eee-159">Minimum supported server</span></span><br/> | <span data-ttu-id="31eee-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31eee-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31eee-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31eee-161">Namespace</span></span><br/>                | <span data-ttu-id="31eee-162">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="31eee-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="31eee-163">MOF</span><span class="sxs-lookup"><span data-stu-id="31eee-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31eee-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31eee-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31eee-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="31eee-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31eee-166">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="31eee-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
