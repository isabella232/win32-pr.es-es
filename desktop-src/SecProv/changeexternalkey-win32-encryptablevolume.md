---
description: Cambia una clave externa que está asociada a un volumen cifrado.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Método ChangeExternalKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688171"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ed22b-103">Método ChangeExternalKey de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="ed22b-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ed22b-104">El método **ChangeExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) cambia una clave externa que está asociada a un volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="ed22b-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed22b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed22b-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="ed22b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed22b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed22b-107">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed22b-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed22b-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="ed22b-108">Type: **string**</span></span>

<span data-ttu-id="ed22b-109">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="ed22b-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="ed22b-110">*NewExternalKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ed22b-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed22b-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ed22b-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="ed22b-112">Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="ed22b-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ed22b-113">*NewVolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed22b-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed22b-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="ed22b-114">Type: **string**</span></span>

<span data-ttu-id="ed22b-115">Un identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="ed22b-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed22b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed22b-116">Return value</span></span>

<span data-ttu-id="ed22b-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed22b-117">Type: **uint32**</span></span>

<span data-ttu-id="ed22b-118">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ed22b-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ed22b-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed22b-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="ed22b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed22b-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed22b-121"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="ed22b-122">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ed22b-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ed22b-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="ed22b-124">El parámetro *NewExternalKey* no es una matriz de tamaño 32.</span><span class="sxs-lookup"><span data-stu-id="ed22b-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ed22b-125"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="ed22b-126">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ed22b-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ed22b-127"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="ed22b-128">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="ed22b-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="ed22b-129">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ed22b-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="ed22b-130"><dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="ed22b-131">En este equipo se encuentra un CD/DVD de arranque.</span><span class="sxs-lookup"><span data-stu-id="ed22b-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="ed22b-132">Quite el CD o el DVD y reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="ed22b-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="ed22b-133"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="ed22b-134">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="ed22b-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="ed22b-135"><dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido</span><span class="sxs-lookup"><span data-stu-id="ed22b-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="ed22b-136">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica" o "clave externa".</span><span class="sxs-lookup"><span data-stu-id="ed22b-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="ed22b-137">Use el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="ed22b-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed22b-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed22b-138">Remarks</span></span>

<span data-ttu-id="ed22b-139">Este método se puede usar para cambiar la clave externa de cualquier protector de clave que use una clave externa.</span><span class="sxs-lookup"><span data-stu-id="ed22b-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed22b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed22b-140">Requirements</span></span>



| <span data-ttu-id="ed22b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed22b-141">Requirement</span></span> | <span data-ttu-id="ed22b-142">Value</span><span class="sxs-lookup"><span data-stu-id="ed22b-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed22b-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed22b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ed22b-144">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed22b-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed22b-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed22b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ed22b-146">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed22b-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed22b-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed22b-147">Namespace</span></span><br/>                | <span data-ttu-id="ed22b-148">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="ed22b-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ed22b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ed22b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed22b-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed22b-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed22b-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed22b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed22b-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="ed22b-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




