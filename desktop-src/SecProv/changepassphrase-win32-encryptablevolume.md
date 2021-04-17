---
description: Usa la nueva frase de contraseña para obtener una nueva clave derivada.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Método ChangePassphrase de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688169"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="da903-103">Método ChangePassphrase de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="da903-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="da903-104">El método **ChangePassphrase** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la nueva frase de contraseña para obtener una nueva clave derivada.</span><span class="sxs-lookup"><span data-stu-id="da903-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="da903-105">Una vez calculada la clave derivada, se usa la nueva clave derivada para proteger la clave maestra del volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="da903-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="da903-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da903-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="da903-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da903-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da903-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da903-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da903-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="da903-109">Type: **string**</span></span>

<span data-ttu-id="da903-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="da903-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="da903-111">*NewPassphrase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da903-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da903-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="da903-112">Type: **string**</span></span>

<span data-ttu-id="da903-113">Cadena actualizada que especifica la frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="da903-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="da903-114">*NewProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da903-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da903-115">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="da903-115">Type: **string**</span></span>

<span data-ttu-id="da903-116">Un identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="da903-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da903-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da903-117">Return value</span></span>

<span data-ttu-id="da903-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da903-118">Type: **uint32**</span></span>

<span data-ttu-id="da903-119">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="da903-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="da903-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da903-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="da903-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="da903-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da903-122"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="da903-123">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="da903-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="da903-124"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="da903-125">El volumen ya está bloqueado por Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da903-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="da903-126">Debe desbloquear la unidad desde el panel de control.</span><span class="sxs-lookup"><span data-stu-id="da903-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="da903-127"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="da903-128">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="da903-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="da903-129">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da903-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="da903-130"><dt>**FVE \_ E \_ SUPERpuesto ( \_ actualización**</dt> <dt>2150694948) (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="da903-131">Otro subproceso actualizó el bloque de control para el volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="da903-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="da903-132"><dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido</span><span class="sxs-lookup"><span data-stu-id="da903-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="da903-133">El protector de clave especificado no es del tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="da903-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="da903-134"><dt>**FVE \_ La longitud de la frase de contraseña de la \_ Directiva E \_ no es \_ \_**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="da903-135">La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.</span><span class="sxs-lookup"><span data-stu-id="da903-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="da903-136"><dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ demasiado \_ simple**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="da903-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="da903-137">La frase de contraseña actualizada no cumple los requisitos de complejidad establecidos por el administrador en la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="da903-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="da903-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da903-138">Requirements</span></span>



| <span data-ttu-id="da903-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="da903-139">Requirement</span></span> | <span data-ttu-id="da903-140">Value</span><span class="sxs-lookup"><span data-stu-id="da903-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da903-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da903-141">Minimum supported client</span></span><br/> | <span data-ttu-id="da903-142">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="da903-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da903-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da903-143">Minimum supported server</span></span><br/> | <span data-ttu-id="da903-144">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="da903-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da903-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da903-145">Namespace</span></span><br/>                | <span data-ttu-id="da903-146">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="da903-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="da903-147">MOF</span><span class="sxs-lookup"><span data-stu-id="da903-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da903-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da903-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da903-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="da903-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da903-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="da903-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




