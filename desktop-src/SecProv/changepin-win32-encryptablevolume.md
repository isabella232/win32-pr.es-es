---
description: Cambia el PIN asociado a un volumen cifrado.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Método ChangePIN de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540950"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d3c45-103">Método ChangePIN de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d3c45-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d3c45-104">El método **ChangePIN** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) cambia el PIN asociado a un volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="d3c45-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="d3c45-105">Si está habilitada la Directiva de grupo "permitir PIN mejorados para el inicio", un PIN puede contener letras, símbolos y espacios, además de números.</span><span class="sxs-lookup"><span data-stu-id="d3c45-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c45-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3c45-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="d3c45-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3c45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c45-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3c45-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c45-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d3c45-109">Type: **string**</span></span>

<span data-ttu-id="d3c45-110">Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="d3c45-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="d3c45-111">*NewPIN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3c45-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c45-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d3c45-112">Type: **string**</span></span>

<span data-ttu-id="d3c45-113">Cadena de identificación personal especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d3c45-113">A user-specified personal identification string.</span></span> <span data-ttu-id="d3c45-114">Esta cadena debe estar formada por una secuencia de 4 a 20 dígitos o, si la Directiva de grupo "permitir PIN mejorados para el inicio" está habilitada, de 4 a 20 letras, símbolos, espacios o números.</span><span class="sxs-lookup"><span data-stu-id="d3c45-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c45-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c45-115">Return value</span></span>

<span data-ttu-id="d3c45-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3c45-116">Type: **uint32**</span></span>

<span data-ttu-id="d3c45-117">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d3c45-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d3c45-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c45-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="d3c45-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3c45-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3c45-120"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="d3c45-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d3c45-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d3c45-122"><dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="d3c45-123">En este equipo se encuentra un CD/DVD de arranque.</span><span class="sxs-lookup"><span data-stu-id="d3c45-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="d3c45-124">Quite el CD o el DVD y reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d3c45-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d3c45-125"><dt>**FVE \_ E \_ \_ \_ caracteres de PIN no válidos**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="d3c45-126">El parámetro *NewPIN* contiene caracteres que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="d3c45-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="d3c45-127">Cuando el directiva de grupo "permitir PIN mejorados para el inicio" está deshabilitado, solo se admiten los números.</span><span class="sxs-lookup"><span data-stu-id="d3c45-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d3c45-128"><dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido</span><span class="sxs-lookup"><span data-stu-id="d3c45-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="d3c45-129">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica" o "clave externa".</span><span class="sxs-lookup"><span data-stu-id="d3c45-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="d3c45-130">Use el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="d3c45-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="d3c45-131"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="d3c45-132">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d3c45-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d3c45-133"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="d3c45-134">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d3c45-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d3c45-135">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d3c45-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="d3c45-136"><dt>**FVE \_ \_Longitud de \_ \_ PIN no \_ válida de la Directiva E**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="d3c45-137">El parámetro *NewPIN* proporcionado tiene más de 20 caracteres, menos de 4 caracteres, o menor que la longitud mínima especificada por directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d3c45-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="d3c45-138"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="d3c45-139">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d3c45-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d3c45-140"><dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="d3c45-141">No se encontró ningún Módulo de plataforma segura compatible (TPM) en este equipo.</span><span class="sxs-lookup"><span data-stu-id="d3c45-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="d3c45-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3c45-142">Remarks</span></span>

<span data-ttu-id="d3c45-143">El método **ChangePIN** crea un nuevo protector de TPM y PIN basado en la información del protector existente y en el PIN recién proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d3c45-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="d3c45-144">El nuevo protector tendrá el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="d3c45-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="d3c45-145">También se puede llamar al método **ChangePIN** para cambiar el PIN de cualquier protector de clave que use un PIN, por ejemplo, TPM y PIN o TPM con PIN y USB.</span><span class="sxs-lookup"><span data-stu-id="d3c45-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="d3c45-146">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3c45-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3c45-147">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d3c45-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d3c45-148">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d3c45-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3c45-149">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d3c45-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c45-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c45-150">Requirements</span></span>



| <span data-ttu-id="d3c45-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c45-151">Requirement</span></span> | <span data-ttu-id="d3c45-152">Value</span><span class="sxs-lookup"><span data-stu-id="d3c45-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c45-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c45-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c45-154">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3c45-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3c45-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c45-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c45-156">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3c45-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3c45-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3c45-157">Namespace</span></span><br/>                | <span data-ttu-id="d3c45-158">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d3c45-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d3c45-159">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c45-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c45-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c45-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c45-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3c45-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c45-162">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d3c45-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
