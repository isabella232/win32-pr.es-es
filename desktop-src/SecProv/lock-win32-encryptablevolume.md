---
description: Desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Método lock de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907809"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bfa06-103">Método lock de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="bfa06-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bfa06-104">El método **Lock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="bfa06-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="bfa06-105">El contenido del volumen permanece inaccesible hasta que se desbloquea mediante el método [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o el método [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa06-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="bfa06-106">Este método no se puede ejecutar correctamente para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="bfa06-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="bfa06-107">Si el disco es compatible con el cifrado de hardware, la banda se establece en "bloqueada".</span><span class="sxs-lookup"><span data-stu-id="bfa06-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bfa06-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfa06-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="bfa06-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfa06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa06-110">*ForceDismount* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bfa06-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa06-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfa06-111">Type: **boolean**</span></span>

<span data-ttu-id="bfa06-112">Si es **true** , el disco se desmontará forzosamente.</span><span class="sxs-lookup"><span data-stu-id="bfa06-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa06-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfa06-113">Return value</span></span>

<span data-ttu-id="bfa06-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfa06-114">Type: **uint32**</span></span>

<span data-ttu-id="bfa06-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="bfa06-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bfa06-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfa06-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="bfa06-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfa06-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfa06-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="bfa06-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bfa06-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="bfa06-120"><dt>**E \_ ACCESO \_ denegado**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="bfa06-121">Las aplicaciones tienen acceso a este volumen.</span><span class="sxs-lookup"><span data-stu-id="bfa06-121">Applications are accessing this volume.</span></span> <span data-ttu-id="bfa06-122">Si todo el acceso no es exclusivo, si se especifica el parámetro *ForceDismount* como true, se permite que el método se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="bfa06-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bfa06-123"><dt>**FVE \_ E \_ no \_ cifrado**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="bfa06-124">El volumen se descifra por completo y no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="bfa06-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="bfa06-125"><dt>**FVE \_ \_Protección E \_ deshabilitada**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="bfa06-126">La clave de cifrado del volumen está disponible en el disco sin cifrar, lo que impide que se bloquee el volumen.</span><span class="sxs-lookup"><span data-stu-id="bfa06-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="bfa06-127"><dt>**FVE \_ E \_ clave de recuperación \_ \_ necesaria**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="bfa06-128">El volumen no tiene protectores de clave del tipo "contraseña numérica" o "clave externa" que son necesarios para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="bfa06-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="bfa06-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfa06-129">Remarks</span></span>

<span data-ttu-id="bfa06-130">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bfa06-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bfa06-131">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bfa06-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bfa06-132">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bfa06-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bfa06-133">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bfa06-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa06-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa06-134">Requirements</span></span>



| <span data-ttu-id="bfa06-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa06-135">Requirement</span></span> | <span data-ttu-id="bfa06-136">Value</span><span class="sxs-lookup"><span data-stu-id="bfa06-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa06-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa06-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa06-138">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfa06-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bfa06-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa06-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa06-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfa06-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfa06-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfa06-141">Namespace</span></span><br/>                | <span data-ttu-id="bfa06-142">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="bfa06-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bfa06-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bfa06-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfa06-144"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfa06-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa06-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa06-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa06-146">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="bfa06-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
