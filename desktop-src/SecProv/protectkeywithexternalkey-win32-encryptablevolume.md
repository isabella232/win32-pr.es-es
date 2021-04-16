---
description: Protege la clave de cifrado del volumen con una clave externa de 256 bits.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Método ProtectKeyWithExternalKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686640"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="24d18-103">Método ProtectKeyWithExternalKey de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="24d18-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="24d18-104">El método **ProtectKeyWithExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen con una clave externa de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="24d18-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="24d18-105">Esta clave externa se puede usar para recuperarse de los errores de autenticación de otros protectores de clave (por ejemplo, TPM).</span><span class="sxs-lookup"><span data-stu-id="24d18-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="24d18-106">Use el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para guardar esta clave externa en un archivo.</span><span class="sxs-lookup"><span data-stu-id="24d18-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="24d18-107">Los dispositivos de memoria USB que contienen esta clave externa se pueden usar como una clave de inicio o una clave de recuperación cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="24d18-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="24d18-108">Se crea un protector de clave de tipo "clave externa" para el volumen.</span><span class="sxs-lookup"><span data-stu-id="24d18-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d18-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24d18-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="24d18-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24d18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d18-111">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24d18-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24d18-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="24d18-112">Type: **string**</span></span>

<span data-ttu-id="24d18-113">Cadena que especifica un identificador asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="24d18-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="24d18-114">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="24d18-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="24d18-115">*ExternalKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24d18-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24d18-116">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="24d18-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="24d18-117">Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="24d18-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="24d18-118">Si no se especifica ninguna clave externa, se genera una de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="24d18-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="24d18-119">Use el método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obtener la clave generada de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="24d18-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="24d18-120">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="24d18-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24d18-121">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="24d18-121">Type: **string**</span></span>

<span data-ttu-id="24d18-122">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="24d18-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="24d18-123">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="24d18-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24d18-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24d18-124">Return value</span></span>

<span data-ttu-id="24d18-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24d18-125">Type: **uint32**</span></span>

<span data-ttu-id="24d18-126">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="24d18-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="24d18-127">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24d18-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="24d18-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="24d18-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24d18-129"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="24d18-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="24d18-130">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="24d18-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="24d18-131"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="24d18-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="24d18-132">Se proporciona el parámetro *ExternalKey* , pero no es una matriz de tamaño 4.</span><span class="sxs-lookup"><span data-stu-id="24d18-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="24d18-133"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="24d18-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="24d18-134">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="24d18-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="24d18-135"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="24d18-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="24d18-136">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="24d18-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="24d18-137">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="24d18-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="24d18-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24d18-138">Remarks</span></span>

<span data-ttu-id="24d18-139">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="24d18-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24d18-140">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="24d18-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="24d18-141">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="24d18-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24d18-142">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="24d18-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24d18-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24d18-143">Requirements</span></span>



| <span data-ttu-id="24d18-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="24d18-144">Requirement</span></span> | <span data-ttu-id="24d18-145">Value</span><span class="sxs-lookup"><span data-stu-id="24d18-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24d18-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24d18-146">Minimum supported client</span></span><br/> | <span data-ttu-id="24d18-147">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="24d18-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24d18-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24d18-148">Minimum supported server</span></span><br/> | <span data-ttu-id="24d18-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="24d18-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24d18-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24d18-150">Namespace</span></span><br/>                | <span data-ttu-id="24d18-151">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="24d18-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="24d18-152">MOF</span><span class="sxs-lookup"><span data-stu-id="24d18-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24d18-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24d18-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d18-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="24d18-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d18-155">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="24d18-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
