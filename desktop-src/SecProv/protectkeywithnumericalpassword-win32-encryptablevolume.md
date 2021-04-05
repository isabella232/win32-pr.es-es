---
description: Protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Método ProtectKeyWithNumericalPassword de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911570"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2a849-103">Método ProtectKeyWithNumericalPassword de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="2a849-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2a849-104">El método **ProtectKeyWithNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial.</span><span class="sxs-lookup"><span data-stu-id="2a849-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="2a849-105">Esta contraseña numérica puede usarse para recuperarse de los errores de autenticación de otros protectores de clave (por ejemplo, TPM).</span><span class="sxs-lookup"><span data-stu-id="2a849-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="2a849-106">Se crea un protector de clave de tipo "contraseña numérica" para el volumen.</span><span class="sxs-lookup"><span data-stu-id="2a849-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="2a849-107">Use el método [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) para validar el formato de la contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="2a849-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a849-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a849-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="2a849-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a849-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a849-110">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a849-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a849-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="2a849-111">Type: **string**</span></span>

<span data-ttu-id="2a849-112">Cadena que especifica un identificador asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="2a849-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="2a849-113">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="2a849-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="2a849-114">*NumericalPassword* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a849-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a849-115">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="2a849-115">Type: **string**</span></span>

<span data-ttu-id="2a849-116">Una cadena que especifica la contraseña numérica de 48 dígitos con formato especial.</span><span class="sxs-lookup"><span data-stu-id="2a849-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="2a849-117">La contraseña numérica debe contener 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="2a849-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="2a849-118">Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo.</span><span class="sxs-lookup"><span data-stu-id="2a849-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="2a849-119">Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser inferior a 720896.</span><span class="sxs-lookup"><span data-stu-id="2a849-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="2a849-120">Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="2a849-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="2a849-121">Los grupos de dígitos se pueden separar opcionalmente con un espacio o un guión.</span><span class="sxs-lookup"><span data-stu-id="2a849-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="2a849-122">Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="2a849-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="2a849-123">Si no se especifica ninguna contraseña numérica, se genera una de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="2a849-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="2a849-124">Use el método [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) para obtener la contraseña generada de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="2a849-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="2a849-125">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2a849-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a849-126">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="2a849-126">Type: **string**</span></span>

<span data-ttu-id="2a849-127">Una cadena que es el identificador único asociado al protector creado y que se puede usar para administrar el protector de clave.</span><span class="sxs-lookup"><span data-stu-id="2a849-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="2a849-128">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="2a849-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a849-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a849-129">Return value</span></span>

<span data-ttu-id="2a849-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a849-130">Type: **uint32**</span></span>

<span data-ttu-id="2a849-131">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a849-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2a849-132">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a849-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2a849-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a849-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a849-134"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="2a849-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2a849-135">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a849-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2a849-136"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="2a849-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="2a849-137">El parámetro *NumericalPassword* no tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="2a849-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="2a849-138"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2a849-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2a849-139">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="2a849-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2a849-140"><dt>**FVE \_ E \_ \_ \_ formato de contraseña no válido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="2a849-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="2a849-141">El parámetro *NumericalPassword* no tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="2a849-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2a849-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a849-142">Remarks</span></span>

<span data-ttu-id="2a849-143">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2a849-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2a849-144">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2a849-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2a849-145">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2a849-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2a849-146">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2a849-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a849-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a849-147">Requirements</span></span>



| <span data-ttu-id="2a849-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a849-148">Requirement</span></span> | <span data-ttu-id="2a849-149">Value</span><span class="sxs-lookup"><span data-stu-id="2a849-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a849-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a849-150">Minimum supported client</span></span><br/> | <span data-ttu-id="2a849-151">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a849-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a849-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a849-152">Minimum supported server</span></span><br/> | <span data-ttu-id="2a849-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a849-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a849-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a849-154">Namespace</span></span><br/>                | <span data-ttu-id="2a849-155">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="2a849-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2a849-156">MOF</span><span class="sxs-lookup"><span data-stu-id="2a849-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a849-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a849-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a849-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a849-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a849-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="2a849-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
