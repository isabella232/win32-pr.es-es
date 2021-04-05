---
description: Quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Método DisableAutoUnlock de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910053"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7b9ae-103">Método DisableAutoUnlock de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="7b9ae-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7b9ae-104">El método **DisableAutoUnlock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando en ese momento, de modo que un volumen de datos no se desbloquee automáticamente cuando se monta, como cuando los dispositivos de memoria extraíbles están conectados al equipo.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="7b9ae-105">Si el desbloqueo automático está deshabilitado o suspendido, se deben usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9ae-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b9ae-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="7b9ae-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b9ae-107">Parameters</span></span>

<span data-ttu-id="7b9ae-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b9ae-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b9ae-109">Return value</span></span>

<span data-ttu-id="7b9ae-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9ae-110">Type: **uint32**</span></span>

<span data-ttu-id="7b9ae-111">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7b9ae-112">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b9ae-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7b9ae-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b9ae-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b9ae-114"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ae-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="7b9ae-115">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7b9ae-116"><dt> **FVE \_ E \_ volumen \_ no \_ enlazado**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ae-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="7b9ae-117">El desbloqueo automático en el volumen está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7b9ae-118"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ae-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="7b9ae-119">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7b9ae-120">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="7b9ae-121"><dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ae-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="7b9ae-122">No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="7b9ae-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b9ae-123">Remarks</span></span>

<span data-ttu-id="7b9ae-124">Si no se devuelve ningún error, este método quita del registro todos los identificadores de protector de volumen y las claves externas usadas para desbloquear automáticamente el volumen.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="7b9ae-125">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7b9ae-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7b9ae-126">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7b9ae-127">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7b9ae-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7b9ae-128">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7b9ae-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9ae-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b9ae-129">Requirements</span></span>



| <span data-ttu-id="7b9ae-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9ae-130">Requirement</span></span> | <span data-ttu-id="7b9ae-131">Value</span><span class="sxs-lookup"><span data-stu-id="7b9ae-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9ae-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b9ae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9ae-133">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b9ae-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b9ae-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b9ae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9ae-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b9ae-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b9ae-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b9ae-136">Namespace</span></span><br/>                | <span data-ttu-id="7b9ae-137">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7b9ae-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7b9ae-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7b9ae-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b9ae-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ae-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9ae-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b9ae-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9ae-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="7b9ae-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
