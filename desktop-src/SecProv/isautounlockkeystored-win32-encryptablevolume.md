---
description: Indica si las claves externas o la información relacionada que se puede usar para desbloquear automáticamente los volúmenes de datos existen en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688150"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="72453-103">Método IsAutoUnlockKeyStored de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="72453-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="72453-104">El método **IsAutoUnlockKeyStored** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si existe cualquier clave externa o información relacionada que pueda usarse para desbloquear automáticamente los volúmenes de datos en el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="72453-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="72453-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72453-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="72453-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72453-107">*IsAutoUnlockKeyStored* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72453-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72453-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="72453-108">Type: **boolean**</span></span>

<span data-ttu-id="72453-109">Es **true** si cualquier información que se pueda utilizar para desbloquear automáticamente los volúmenes de datos se almacena en el registro del volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="72453-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72453-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72453-110">Return value</span></span>

<span data-ttu-id="72453-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72453-111">Type: **uint32**</span></span>

<span data-ttu-id="72453-112">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="72453-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="72453-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72453-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="72453-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="72453-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72453-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="72453-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="72453-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="72453-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="72453-117"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="72453-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="72453-118">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="72453-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="72453-119">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72453-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="72453-120"><dt>**FVE \_ E \_ no es el \_ \_ volumen de sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="72453-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="72453-121">El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="72453-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="72453-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72453-122">Remarks</span></span>

<span data-ttu-id="72453-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para quitar toda la información de desbloqueo del volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="72453-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="72453-124">La información que se usa para desbloquear un volumen se almacena cuando se ejecuta [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para un volumen de datos mientras se ejecuta el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="72453-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="72453-125">**IsAutoUnlockKeyStored** difiere de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) en que, aunque el desbloqueo automático esté deshabilitado para todos los volúmenes de datos conectados actualmente al equipo, puede que todavía esté desbloqueando la información asociada a los volúmenes de datos desconectados o volúmenes de datos que ya no existen.</span><span class="sxs-lookup"><span data-stu-id="72453-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="72453-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="72453-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72453-127">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="72453-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="72453-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="72453-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72453-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="72453-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72453-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72453-130">Requirements</span></span>



| <span data-ttu-id="72453-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="72453-131">Requirement</span></span> | <span data-ttu-id="72453-132">Value</span><span class="sxs-lookup"><span data-stu-id="72453-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72453-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72453-133">Minimum supported client</span></span><br/> | <span data-ttu-id="72453-134">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="72453-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="72453-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72453-135">Minimum supported server</span></span><br/> | <span data-ttu-id="72453-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="72453-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72453-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72453-137">Namespace</span></span><br/>                | <span data-ttu-id="72453-138">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="72453-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="72453-139">MOF</span><span class="sxs-lookup"><span data-stu-id="72453-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72453-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72453-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72453-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="72453-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72453-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="72453-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
