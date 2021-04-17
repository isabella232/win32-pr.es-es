---
description: Exporta información que puede ayudar a proteger los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688158"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="cb409-103">Método GetKeyPackage de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="cb409-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="cb409-104">El método **GetKeyPackage** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) exporta información que puede ayudar a proteger los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.</span><span class="sxs-lookup"><span data-stu-id="cb409-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="cb409-105">La información exportada se compone de la clave de cifrado del volumen protegida por un protector de clave del tipo "contraseña numérica" o "clave externa".</span><span class="sxs-lookup"><span data-stu-id="cb409-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="cb409-106">Para hacer uso de este paquete, también debe guardar la contraseña numérica correspondiente o la clave externa.</span><span class="sxs-lookup"><span data-stu-id="cb409-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb409-107">Si decide exportar un paquete de claves, asegúrese de mantener esta información en una ubicación bien protegida.</span><span class="sxs-lookup"><span data-stu-id="cb409-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="cb409-108">No lleve esta información al equipo.</span><span class="sxs-lookup"><span data-stu-id="cb409-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="cb409-109">Si este paquete de claves se pierde o se lo roban, deberá descifrar el volumen y volver a cifrarlo mediante una nueva clave.</span><span class="sxs-lookup"><span data-stu-id="cb409-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="cb409-110">En caso de que se produzca un error en la unidad, existe la herramienta de reparación de BitLocker para ayudar a salvar los datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="cb409-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="cb409-111">Para obtener más información sobre cómo esta herramienta puede usar el paquete de claves, consulte [Cómo usar la herramienta de reparación de BitLocker para ayudar a recuperar datos de un volumen cifrado en Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="cb409-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb409-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb409-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="cb409-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb409-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb409-114">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb409-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb409-115">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="cb409-115">Type: **string**</span></span>

<span data-ttu-id="cb409-116">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="cb409-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="cb409-117">Para exportar un paquete de claves, debe usar un protector de clave de tipo "contraseña numérica" o "clave externa".</span><span class="sxs-lookup"><span data-stu-id="cb409-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="cb409-118">*\[ KeyPackage \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="cb409-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb409-119">Tipo: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cb409-119">Type: **uint8**</span></span>

<span data-ttu-id="cb409-120">Secuencia de bytes que contiene la clave de cifrado para un volumen, protegida por el protector de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="cb409-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb409-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb409-121">Return value</span></span>

<span data-ttu-id="cb409-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb409-122">Type: **uint32**</span></span>

<span data-ttu-id="cb409-123">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cb409-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="cb409-124">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb409-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="cb409-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb409-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb409-126"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="cb409-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="cb409-127">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cb409-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="cb409-128"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="cb409-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="cb409-129">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cb409-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="cb409-130"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="cb409-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="cb409-131">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="cb409-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="cb409-132">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cb409-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="cb409-133"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="cb409-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="cb409-134">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="cb409-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="cb409-135"><dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido</span><span class="sxs-lookup"><span data-stu-id="cb409-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="cb409-136">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica" o "clave externa".</span><span class="sxs-lookup"><span data-stu-id="cb409-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="cb409-137">Use el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="cb409-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb409-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb409-138">Remarks</span></span>

<span data-ttu-id="cb409-139">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cb409-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cb409-140">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cb409-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cb409-141">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="cb409-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cb409-142">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="cb409-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb409-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb409-143">Requirements</span></span>



| <span data-ttu-id="cb409-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb409-144">Requirement</span></span> | <span data-ttu-id="cb409-145">Value</span><span class="sxs-lookup"><span data-stu-id="cb409-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb409-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb409-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cb409-147">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb409-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cb409-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb409-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cb409-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb409-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb409-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb409-150">Namespace</span></span><br/>                | <span data-ttu-id="cb409-151">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="cb409-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="cb409-152">MOF</span><span class="sxs-lookup"><span data-stu-id="cb409-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb409-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb409-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb409-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb409-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb409-155">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="cb409-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
