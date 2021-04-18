---
description: Quita todas las claves externas y la información relacionada guardadas en el volumen del sistema operativo que se está ejecutando actualmente y que se usan para desbloquear automáticamente los volúmenes de datos.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686662"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="01b0a-103">Método ClearAllAutoUnlockKeys de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="01b0a-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="01b0a-104">El método **ClearAllAutoUnlockKeys** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita todas las claves externas y la información relacionada guardadas en el volumen del sistema operativo que se está ejecutando actualmente y que se usan para desbloquear automáticamente los volúmenes de datos.</span><span class="sxs-lookup"><span data-stu-id="01b0a-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01b0a-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="01b0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01b0a-106">Parameters</span></span>

<span data-ttu-id="01b0a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="01b0a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01b0a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01b0a-108">Return value</span></span>

<span data-ttu-id="01b0a-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01b0a-109">Type: **uint32**</span></span>

<span data-ttu-id="01b0a-110">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="01b0a-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="01b0a-111">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01b0a-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="01b0a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="01b0a-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01b0a-113"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="01b0a-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="01b0a-114">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="01b0a-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="01b0a-115"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="01b0a-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="01b0a-116">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="01b0a-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="01b0a-117">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01b0a-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="01b0a-118"><dt>**FVE \_ E \_ no es el \_ \_ volumen de sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="01b0a-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="01b0a-119">El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="01b0a-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="01b0a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01b0a-120">Remarks</span></span>

<span data-ttu-id="01b0a-121">**ClearAllAutoUnlockKeys** logra la misma funcionalidad que la ejecución de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para cada volumen de datos que se haya asociado al sistema operativo que se está ejecutando en ese momento, incluso a los volúmenes de datos que no están conectados al equipo.</span><span class="sxs-lookup"><span data-stu-id="01b0a-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="01b0a-122">También quita cualquier información de desbloqueo obsoleta asociada a los volúmenes de datos que ya no existen.</span><span class="sxs-lookup"><span data-stu-id="01b0a-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="01b0a-123">Antes de llamar a [**descifrado**](decrypt-win32-encryptablevolume.md) en el volumen del sistema operativo que se está ejecutando actualmente, use **ClearAllAutoUnlockKeys** para asegurarse de que no se pueda tener acceso a la información colocada en el registro del sistema operativo para desbloquear automáticamente los volúmenes de datos sin cifrar en el disco.</span><span class="sxs-lookup"><span data-stu-id="01b0a-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="01b0a-124">Una vez que **ClearAllAutoUnlockKeys** se ejecuta correctamente, se pueden usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear todos los volúmenes de datos de este equipo.</span><span class="sxs-lookup"><span data-stu-id="01b0a-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="01b0a-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para volver a habilitar el desbloqueo automático de un volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="01b0a-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="01b0a-126">Si no se devuelve ningún otro error, **ClearAllAutoUnlockKeys** quita del registro todos los identificadores de protector de volumen y las claves externas usadas para desbloquear automáticamente cualquier volumen de datos que se haya asociado al volumen del sistema operativo que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="01b0a-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="01b0a-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="01b0a-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01b0a-128">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="01b0a-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="01b0a-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="01b0a-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01b0a-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="01b0a-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01b0a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b0a-131">Requirements</span></span>



| <span data-ttu-id="01b0a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b0a-132">Requirement</span></span> | <span data-ttu-id="01b0a-133">Value</span><span class="sxs-lookup"><span data-stu-id="01b0a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b0a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b0a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="01b0a-135">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="01b0a-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01b0a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01b0a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="01b0a-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="01b0a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01b0a-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01b0a-138">Namespace</span></span><br/>                | <span data-ttu-id="01b0a-139">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="01b0a-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="01b0a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="01b0a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01b0a-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01b0a-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b0a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="01b0a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b0a-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="01b0a-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
