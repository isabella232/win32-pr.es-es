---
description: Usa una contraseña numérica proporcionada para tener acceso al contenido de un volumen de datos.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907803"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="478df-103">Método UnlockWithNumericalPassword de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="478df-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="478df-104">El método **UnlockWithNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una contraseña numérica proporcionada para tener acceso al contenido de un volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="478df-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="478df-105">La clave de cifrado del volumen debe estar protegida con uno o varios protectores de clave del tipo "contraseña numérica" (mediante el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) para poder desbloquear el volumen con este método.</span><span class="sxs-lookup"><span data-stu-id="478df-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="478df-106">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="478df-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="478df-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="478df-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="478df-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="478df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478df-109">*NumericalPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="478df-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478df-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="478df-110">Type: **string**</span></span>

<span data-ttu-id="478df-111">Cadena que especifica la contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="478df-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="478df-112">La contraseña numérica debe contener 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="478df-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="478df-113">Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo.</span><span class="sxs-lookup"><span data-stu-id="478df-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="478df-114">Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser inferior a 65536.</span><span class="sxs-lookup"><span data-stu-id="478df-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="478df-115">Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="478df-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="478df-116">Los grupos de dígitos se pueden separar opcionalmente con un espacio o un guión.</span><span class="sxs-lookup"><span data-stu-id="478df-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="478df-117">Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="478df-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478df-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="478df-118">Return value</span></span>

<span data-ttu-id="478df-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="478df-119">Type: **uint32**</span></span>

<span data-ttu-id="478df-120">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="478df-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="478df-121">Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="478df-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="478df-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="478df-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="478df-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="478df-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="478df-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="478df-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="478df-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="478df-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="478df-126"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="478df-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="478df-127">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="478df-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="478df-128">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="478df-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="478df-129"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="478df-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="478df-130">El volumen no tiene un protector de clave del tipo "contraseña numérica".</span><span class="sxs-lookup"><span data-stu-id="478df-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="478df-131">El parámetro *NumericalPassword* tiene un formato válido, pero no se puede usar una contraseña numérica para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="478df-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="478df-132"><dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="478df-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="478df-133">El parámetro *NumericalPassword* no puede desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="478df-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="478df-134">Uno o varios protectores de clave del tipo "contraseña numérica" existen, pero el parámetro *NumericalPassword* especificado no puede desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="478df-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="478df-135"><dt>**FVE \_ E \_ \_ \_ formato de contraseña no válido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="478df-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="478df-136">El parámetro *NumericalPassword* no tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="478df-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="478df-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="478df-137">Remarks</span></span>

<span data-ttu-id="478df-138">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="478df-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="478df-139">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="478df-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="478df-140">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="478df-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="478df-141">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="478df-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="478df-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="478df-142">Requirements</span></span>



| <span data-ttu-id="478df-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="478df-143">Requirement</span></span> | <span data-ttu-id="478df-144">Value</span><span class="sxs-lookup"><span data-stu-id="478df-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478df-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="478df-145">Minimum supported client</span></span><br/> | <span data-ttu-id="478df-146">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="478df-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="478df-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="478df-147">Minimum supported server</span></span><br/> | <span data-ttu-id="478df-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="478df-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="478df-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="478df-149">Namespace</span></span><br/>                | <span data-ttu-id="478df-150">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="478df-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="478df-151">MOF</span><span class="sxs-lookup"><span data-stu-id="478df-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="478df-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="478df-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="478df-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="478df-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478df-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="478df-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
