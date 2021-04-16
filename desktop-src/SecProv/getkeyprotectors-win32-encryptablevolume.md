---
description: Enumera los protectores usados para proteger la clave de cifrado del volumen.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Método GetKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686649"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="32e42-103">Método GetKeyProtectors de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="32e42-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="32e42-104">El método **GetKeyProtectors** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera los protectores usados para proteger la clave de cifrado del volumen.</span><span class="sxs-lookup"><span data-stu-id="32e42-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="32e42-105">Si se proporciona un tipo de protector, solo se devuelven los protectores de clave de volumen del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="32e42-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e42-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32e42-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="32e42-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32e42-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e42-108">*KeyProtectorType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="32e42-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32e42-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32e42-109">Type: **uint32**</span></span>

<span data-ttu-id="32e42-110">Entero sin signo que especifica el tipo de protector de clave que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="32e42-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="32e42-111">Si no se especifica este parámetro, se devuelven todos los protectores de clave disponibles del volumen.</span><span class="sxs-lookup"><span data-stu-id="32e42-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="32e42-112">Value</span><span class="sxs-lookup"><span data-stu-id="32e42-112">Value</span></span>                                                                         | <span data-ttu-id="32e42-113">Significado</span><span class="sxs-lookup"><span data-stu-id="32e42-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="32e42-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="32e42-115">Todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="32e42-115">All types.</span></span><br/> <span data-ttu-id="32e42-116">Se devuelven todos los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="32e42-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="32e42-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="32e42-118">Módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="32e42-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="32e42-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="32e42-120">Clave externa.</span><span class="sxs-lookup"><span data-stu-id="32e42-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="32e42-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="32e42-122">Contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="32e42-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="32e42-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="32e42-124">TPM y PIN.</span><span class="sxs-lookup"><span data-stu-id="32e42-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="32e42-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="32e42-126">TPM y clave de inicio.</span><span class="sxs-lookup"><span data-stu-id="32e42-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="32e42-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="32e42-128">TPM y clave de inicio y PIN.</span><span class="sxs-lookup"><span data-stu-id="32e42-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="32e42-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="32e42-130">Clave pública.</span><span class="sxs-lookup"><span data-stu-id="32e42-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="32e42-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="32e42-132">Frase.</span><span class="sxs-lookup"><span data-stu-id="32e42-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="32e42-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="32e42-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="32e42-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="32e42-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="32e42-136">Identificador de seguridad (SID)</span><span class="sxs-lookup"><span data-stu-id="32e42-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="32e42-137">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32e42-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32e42-138">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="32e42-138">Type: **string\[\]**</span></span>

<span data-ttu-id="32e42-139">Matriz de cadenas que identifican los protectores de clave usados para proteger la clave de cifrado del volumen.</span><span class="sxs-lookup"><span data-stu-id="32e42-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e42-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32e42-140">Return value</span></span>

<span data-ttu-id="32e42-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32e42-141">Type: **uint32**</span></span>

<span data-ttu-id="32e42-142">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="32e42-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="32e42-143">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32e42-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="32e42-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="32e42-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32e42-145"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="32e42-146">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="32e42-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="32e42-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="32e42-148">Se ha especificado el parámetro *VolumeKeyProtectorID* pero no hace referencia a un *KeyProtectorType* válido.</span><span class="sxs-lookup"><span data-stu-id="32e42-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="32e42-149"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="32e42-150">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="32e42-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="32e42-151">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="32e42-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="32e42-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32e42-152">Remarks</span></span>

<span data-ttu-id="32e42-153">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="32e42-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="32e42-154">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="32e42-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="32e42-155">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="32e42-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="32e42-156">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="32e42-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32e42-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e42-157">Requirements</span></span>



| <span data-ttu-id="32e42-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e42-158">Requirement</span></span> | <span data-ttu-id="32e42-159">Value</span><span class="sxs-lookup"><span data-stu-id="32e42-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e42-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e42-160">Minimum supported client</span></span><br/> | <span data-ttu-id="32e42-161">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="32e42-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="32e42-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e42-162">Minimum supported server</span></span><br/> | <span data-ttu-id="32e42-163">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="32e42-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32e42-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32e42-164">Namespace</span></span><br/>                | <span data-ttu-id="32e42-165">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="32e42-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="32e42-166">MOF</span><span class="sxs-lookup"><span data-stu-id="32e42-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e42-167"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e42-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e42-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e42-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e42-169">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="32e42-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
