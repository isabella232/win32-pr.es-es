---
description: 'Método UnlockWithPassphrase de la clase Win32_EncryptableVolume : usa la frase de contraseña para obtener la clave derivada.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116463"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="df061-103">Método UnlockWithPassphrase de la clase EncryptableVolume de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="df061-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="df061-104">El **método UnlockWithPassphrase** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada.</span><span class="sxs-lookup"><span data-stu-id="df061-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="df061-105">Una vez calculada la clave derivada, se usa la clave derivada para desbloquear la clave maestra del volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="df061-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="df061-106">Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""</span><span class="sxs-lookup"><span data-stu-id="df061-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="df061-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df061-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="df061-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df061-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df061-109">*Frase de contraseña* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="df061-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df061-110">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="df061-110">Type: **string**</span></span>

<span data-ttu-id="df061-111">Cadena que especifica la frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="df061-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df061-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df061-112">Return value</span></span>

<span data-ttu-id="df061-113">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="df061-113">Type: **uint32**</span></span>

<span data-ttu-id="df061-114">Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="df061-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="df061-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df061-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="df061-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="df061-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df061-117"><dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="df061-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="df061-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="df061-119"><dt>**FVE \_ E \_ NO \_ ACTIVADO**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="df061-120">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="df061-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="df061-121">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="df061-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="df061-122"><dt>**FVE \_ E \_ FIPS \_ EVITA LA FRASE \_ DE CONTRASEÑA**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="df061-123">La configuración de directiva de grupo que requiere el cumplimiento de FIPS impedía que la frase de contraseña se generara o usara.</span><span class="sxs-lookup"><span data-stu-id="df061-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="df061-124"><dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="df061-125">La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.</span><span class="sxs-lookup"><span data-stu-id="df061-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="df061-126"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="df061-127">La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="df061-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="df061-128"><dt>**FVE \_ E \_ ERROR \_ DE AUTENTICACIÓN**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="df061-129">El volumen no se puede desbloquear con la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="df061-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="df061-130"><dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="df061-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="df061-131">El protector de clave proporcionado no existe en el volumen.</span><span class="sxs-lookup"><span data-stu-id="df061-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="df061-132">Debe escribir otro protector de clave.</span><span class="sxs-lookup"><span data-stu-id="df061-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="df061-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df061-133">Requirements</span></span>



| <span data-ttu-id="df061-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="df061-134">Requirement</span></span> | <span data-ttu-id="df061-135">Valor</span><span class="sxs-lookup"><span data-stu-id="df061-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df061-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df061-136">Minimum supported client</span></span><br/> | <span data-ttu-id="df061-137">Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="df061-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df061-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df061-138">Minimum supported server</span></span><br/> | <span data-ttu-id="df061-139">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="df061-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df061-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df061-140">Namespace</span></span><br/>                | <span data-ttu-id="df061-141">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="df061-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="df061-142">MOF</span><span class="sxs-lookup"><span data-stu-id="df061-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df061-143"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="df061-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df061-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df061-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df061-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="df061-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




