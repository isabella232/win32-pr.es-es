---
description: Usa la frase de contraseña para obtener la clave derivada.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668468"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="cbf27-103">Método UnlockWithPassphrase de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="cbf27-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="cbf27-104">El método **UnlockWithPassphrase** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada.</span><span class="sxs-lookup"><span data-stu-id="cbf27-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="cbf27-105">Una vez calculada la clave derivada, se usa la clave derivada para desbloquear la clave maestra del volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="cbf27-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="cbf27-106">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="cbf27-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cbf27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbf27-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="cbf27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbf27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf27-109">*Frase de contraseña* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cbf27-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf27-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="cbf27-110">Type: **string**</span></span>

<span data-ttu-id="cbf27-111">Cadena que especifica la frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="cbf27-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf27-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbf27-112">Return value</span></span>

<span data-ttu-id="cbf27-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbf27-113">Type: **uint32**</span></span>

<span data-ttu-id="cbf27-114">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cbf27-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="cbf27-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbf27-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="cbf27-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf27-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbf27-117"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="cbf27-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cbf27-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="cbf27-119"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="cbf27-120">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="cbf27-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="cbf27-121">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbf27-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="cbf27-122"><dt>**FVE \_ E \_ FIPS \_ evita la \_ frase de contraseña**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="cbf27-123">La configuración de directiva de grupo que requiere el cumplimiento de FIPS impidió la generación o el uso de la frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="cbf27-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="cbf27-124"><dt>**FVE \_ La longitud de la frase de contraseña de la \_ Directiva E \_ no es \_ \_**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="cbf27-125">La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.</span><span class="sxs-lookup"><span data-stu-id="cbf27-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="cbf27-126"><dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ demasiado \_ simple**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="cbf27-127">La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="cbf27-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="cbf27-128"><dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="cbf27-129">No se puede desbloquear el volumen con la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="cbf27-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="cbf27-130"><dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="cbf27-131">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="cbf27-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="cbf27-132">Debe especificar otro protector de clave.</span><span class="sxs-lookup"><span data-stu-id="cbf27-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="cbf27-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbf27-133">Requirements</span></span>



| <span data-ttu-id="cbf27-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf27-134">Requirement</span></span> | <span data-ttu-id="cbf27-135">Value</span><span class="sxs-lookup"><span data-stu-id="cbf27-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf27-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf27-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf27-137">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="cbf27-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cbf27-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf27-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf27-139">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbf27-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbf27-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cbf27-140">Namespace</span></span><br/>                | <span data-ttu-id="cbf27-141">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="cbf27-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="cbf27-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cbf27-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbf27-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbf27-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf27-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbf27-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf27-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="cbf27-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




