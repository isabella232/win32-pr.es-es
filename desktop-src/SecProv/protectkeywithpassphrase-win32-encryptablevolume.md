---
description: 'Método ProtectKeyWithPassphrase de la clase Win32_EncryptableVolume: usa la frase de contraseña para obtener la clave derivada.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098353"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="34aef-103">Método ProtectKeyWithPassphrase de la clase EncryptableVolume de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="34aef-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="34aef-104">El **método ProtectKeyWithPassphrase** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada.</span><span class="sxs-lookup"><span data-stu-id="34aef-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="34aef-105">Una vez calculada la clave derivada, la clave derivada se usa para proteger la clave maestra del volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="34aef-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="34aef-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34aef-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="34aef-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34aef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34aef-108">*FriendlyName* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="34aef-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34aef-109">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34aef-109">Type: **string**</span></span>

<span data-ttu-id="34aef-110">Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="34aef-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="34aef-111">Si no se especifica este parámetro, se usa un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="34aef-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="34aef-112">*Frase de contraseña* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="34aef-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34aef-113">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34aef-113">Type: **string**</span></span>

<span data-ttu-id="34aef-114">Cadena que especifica la frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="34aef-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="34aef-115">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34aef-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34aef-116">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34aef-116">Type: **string**</span></span>

<span data-ttu-id="34aef-117">Cadena que identifica de forma única el protector de clave creado.</span><span class="sxs-lookup"><span data-stu-id="34aef-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="34aef-118">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.</span><span class="sxs-lookup"><span data-stu-id="34aef-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34aef-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34aef-119">Return value</span></span>

<span data-ttu-id="34aef-120">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="34aef-120">Type: **uint32**</span></span>

<span data-ttu-id="34aef-121">Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="34aef-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="34aef-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34aef-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="34aef-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="34aef-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34aef-124"><dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="34aef-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="34aef-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="34aef-126"><dt>**FVE \_ E \_ NO SE PERMITE EN MODO \_ \_ \_ \_ SEGURO**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="34aef-127">Cifrado de unidad BitLocker solo se puede usar con fines de recuperación cuando se usa en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="34aef-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="34aef-128"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ NOT \_ ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="34aef-129">La directiva de grupo no permite la creación de una frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="34aef-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="34aef-130"><dt>**FVE \_ E \_ FIPS \_ EVITA LA FRASE \_ DE CONTRASEÑA**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="34aef-131">La configuración de directiva de grupo que requiere el cumplimiento de FIPS impedía que la frase de contraseña se generara o usara.</span><span class="sxs-lookup"><span data-stu-id="34aef-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="34aef-132"><dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="34aef-133">La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.</span><span class="sxs-lookup"><span data-stu-id="34aef-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="34aef-134"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="34aef-135">La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="34aef-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="34aef-136"><dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="34aef-137">El volumen ya está bloqueado por Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34aef-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="34aef-138">Debe desbloquear la unidad desde Panel de control.</span><span class="sxs-lookup"><span data-stu-id="34aef-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="34aef-139"><dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="34aef-140">Otro subproceso actualizó el bloque de control para el volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="34aef-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="34aef-141"><dt>**FVE \_ E \_ KEY PROTECTOR NOT \_ \_ \_ SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="34aef-142">El protector de clave no es compatible con la versión de Cifrado de unidad BitLocker actualmente en el volumen.</span><span class="sxs-lookup"><span data-stu-id="34aef-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="34aef-143"><dt>**FVE \_ E \_ NO SE PERMITE LA \_ \_ FRASE \_ \_**</dt> DE CONTRASEÑA DEL VOLUMEN DEL SISTEMA OPERATIVO <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="34aef-144">La frase de contraseña no se puede agregar al volumen del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="34aef-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="34aef-145"><dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="34aef-146">El protector de clave proporcionado ya existe en este volumen.</span><span class="sxs-lookup"><span data-stu-id="34aef-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="34aef-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34aef-147">Requirements</span></span>



| <span data-ttu-id="34aef-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="34aef-148">Requirement</span></span> | <span data-ttu-id="34aef-149">Valor</span><span class="sxs-lookup"><span data-stu-id="34aef-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34aef-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34aef-150">Minimum supported client</span></span><br/> | <span data-ttu-id="34aef-151">Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="34aef-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34aef-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34aef-152">Minimum supported server</span></span><br/> | <span data-ttu-id="34aef-153">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="34aef-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34aef-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34aef-154">Namespace</span></span><br/>                | <span data-ttu-id="34aef-155">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="34aef-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="34aef-156">MOF</span><span class="sxs-lookup"><span data-stu-id="34aef-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34aef-157"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="34aef-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34aef-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34aef-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34aef-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="34aef-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




