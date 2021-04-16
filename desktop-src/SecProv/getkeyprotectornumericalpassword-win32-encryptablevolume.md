---
description: Recupera la contraseña numérica de un protector de clave determinado.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Método GetKeyProtectorNumericalPassword de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686650"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="43fa3-103">Método GetKeyProtectorNumericalPassword de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="43fa3-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="43fa3-104">El método **GetKeyProtectorNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la contraseña numérica de un protector de clave determinado del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="43fa3-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="43fa3-105">El identificador de protector de clave debe hacer referencia a un protector de clave de tipo "contraseña numérica".</span><span class="sxs-lookup"><span data-stu-id="43fa3-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="43fa3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43fa3-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="43fa3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43fa3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fa3-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43fa3-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="43fa3-109">Type: **string**</span></span>

<span data-ttu-id="43fa3-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="43fa3-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="43fa3-111">*NumericalPassword* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43fa3-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="43fa3-112">Type: **string**</span></span>

<span data-ttu-id="43fa3-113">Cadena que representa la contraseña que se puede usar para desbloquear el volumen correspondiente.</span><span class="sxs-lookup"><span data-stu-id="43fa3-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="43fa3-114">La contraseña numérica tiene 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="43fa3-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="43fa3-115">Estos dígitos se dividen en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo.</span><span class="sxs-lookup"><span data-stu-id="43fa3-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="43fa3-116">Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="43fa3-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="43fa3-117">Los grupos de dígitos se separan con un guión.</span><span class="sxs-lookup"><span data-stu-id="43fa3-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="43fa3-118">Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" es el formato de la contraseña devuelta.</span><span class="sxs-lookup"><span data-stu-id="43fa3-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fa3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43fa3-119">Return value</span></span>

<span data-ttu-id="43fa3-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43fa3-120">Type: **uint32**</span></span>

<span data-ttu-id="43fa3-121">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="43fa3-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="43fa3-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43fa3-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="43fa3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="43fa3-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43fa3-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="43fa3-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="43fa3-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="43fa3-126"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="43fa3-127">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="43fa3-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="43fa3-128"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="43fa3-129">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica".</span><span class="sxs-lookup"><span data-stu-id="43fa3-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="43fa3-130"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="43fa3-131">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="43fa3-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="43fa3-132">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="43fa3-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="43fa3-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43fa3-133">Remarks</span></span>

<span data-ttu-id="43fa3-134">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="43fa3-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="43fa3-135">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="43fa3-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="43fa3-136">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="43fa3-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="43fa3-137">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="43fa3-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43fa3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43fa3-138">Requirements</span></span>



| <span data-ttu-id="43fa3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fa3-139">Requirement</span></span> | <span data-ttu-id="43fa3-140">Value</span><span class="sxs-lookup"><span data-stu-id="43fa3-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43fa3-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43fa3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="43fa3-142">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="43fa3-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43fa3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="43fa3-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43fa3-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43fa3-145">Namespace</span></span><br/>                | <span data-ttu-id="43fa3-146">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="43fa3-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="43fa3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="43fa3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43fa3-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43fa3-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="43fa3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fa3-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="43fa3-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
