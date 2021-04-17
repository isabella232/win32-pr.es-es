---
description: Indica si el contenido del volumen es accesible desde Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Método GetLockStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686648"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5c0b3-103">Método GetLockStatus de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="5c0b3-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5c0b3-104">El método **GetLockStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el contenido del volumen es accesible desde Windows.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c0b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c0b3-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5c0b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c0b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c0b3-107">*LockStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5c0b3-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c0b3-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c0b3-108">Type: **uint32**</span></span>

<span data-ttu-id="5c0b3-109">Especifica si el contenido del volumen es accesible desde Windows.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="5c0b3-110">Value</span><span class="sxs-lookup"><span data-stu-id="5c0b3-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="5c0b3-111">Significado</span><span class="sxs-lookup"><span data-stu-id="5c0b3-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="5c0b3-112"><dt>**Desbloqueado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5c0b3-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="5c0b3-113">Para una unidad de disco duro estándar:</span><span class="sxs-lookup"><span data-stu-id="5c0b3-113">For a standard HDD:</span></span><br/> <span data-ttu-id="5c0b3-114">Se puede tener acceso al contenido completo del volumen.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="5c0b3-115">Un volumen desbloqueado es totalmente descifrado o tiene la clave de cifrado disponible en el disco sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="5c0b3-116">El volumen que contiene el sistema operativo en ejecución actual (por ejemplo, el volumen de Windows en ejecución) siempre es accesible y no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="5c0b3-117">Para un EHDD:</span><span class="sxs-lookup"><span data-stu-id="5c0b3-117">For an EHDD:</span></span><br/> <span data-ttu-id="5c0b3-118">La banda se desbloquea de forma perpetua.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="5c0b3-119"><dt>**Bloqueado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c0b3-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="5c0b3-120">Para una unidad de disco duro estándar:</span><span class="sxs-lookup"><span data-stu-id="5c0b3-120">For a standard HDD:</span></span><br/> <span data-ttu-id="5c0b3-121">No se puede tener acceso a todo o una parte del contenido del volumen.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="5c0b3-122">Un volumen bloqueado debe estar cifrado parcial o totalmente y no debe tener la clave de cifrado disponible en el disco sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="5c0b3-123">Para un EHDD:</span><span class="sxs-lookup"><span data-stu-id="5c0b3-123">For an EHDD:</span></span><br/> <span data-ttu-id="5c0b3-124">La banda está desbloqueada o bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c0b3-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c0b3-125">Return value</span></span>

<span data-ttu-id="5c0b3-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c0b3-126">Type: **uint32**</span></span>

<span data-ttu-id="5c0b3-127">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5c0b3-128">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c0b3-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5c0b3-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0b3-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5c0b3-130"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0b3-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5c0b3-131">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c0b3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c0b3-132">Remarks</span></span>

<span data-ttu-id="5c0b3-133">Use [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) y [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para obtener acceso al contenido del volumen.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="5c0b3-134">Use el método [**Lock**](lock-win32-encryptablevolume.md) para ceder el acceso al contenido del volumen.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="5c0b3-135">El volumen que contiene el sistema operativo que se está ejecutando actualmente siempre es accesible y no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="5c0b3-136">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5c0b3-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5c0b3-137">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5c0b3-138">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5c0b3-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5c0b3-139">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5c0b3-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c0b3-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c0b3-140">Requirements</span></span>



| <span data-ttu-id="5c0b3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c0b3-141">Requirement</span></span> | <span data-ttu-id="5c0b3-142">Value</span><span class="sxs-lookup"><span data-stu-id="5c0b3-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0b3-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c0b3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5c0b3-144">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c0b3-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5c0b3-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c0b3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5c0b3-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c0b3-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c0b3-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c0b3-147">Namespace</span></span><br/>                | <span data-ttu-id="5c0b3-148">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="5c0b3-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5c0b3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5c0b3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c0b3-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c0b3-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c0b3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c0b3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0b3-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="5c0b3-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
