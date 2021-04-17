---
description: Elimina todos los protectores de clave para el volumen.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687571"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="726bb-103">Método DeleteKeyProtectors de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="726bb-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="726bb-104">El método **DeleteKeyProtectors** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina todos los protectores de clave para el volumen.</span><span class="sxs-lookup"><span data-stu-id="726bb-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="726bb-105">Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtectors** se ejecuta correctamente, el volumen se revierte a un sistema de archivos NTFS estándar.</span><span class="sxs-lookup"><span data-stu-id="726bb-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="726bb-106">Si el volumen no se ha descifrado completamente, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de ejecutar **DeleteKeyProtectors** para asegurarse de que las partes cifradas del volumen permanecen accesibles.</span><span class="sxs-lookup"><span data-stu-id="726bb-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="726bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="726bb-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="726bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="726bb-108">Parameters</span></span>

<span data-ttu-id="726bb-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="726bb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="726bb-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="726bb-110">Return value</span></span>

<span data-ttu-id="726bb-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="726bb-111">Type: **uint32**</span></span>

<span data-ttu-id="726bb-112">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="726bb-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="726bb-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="726bb-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="726bb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="726bb-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="726bb-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="726bb-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="726bb-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="726bb-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="726bb-117"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="726bb-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="726bb-118">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="726bb-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="726bb-119"><dt>**FVE \_ E \_ clave \_ necesaria**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="726bb-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="726bb-120">No se puede quitar el último protector de clave para un volumen totalmente cifrado o parcial si están habilitados los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="726bb-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="726bb-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar este protector de clave más reciente para asegurarse de que las partes cifradas del volumen sigan siendo accesibles.</span><span class="sxs-lookup"><span data-stu-id="726bb-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="726bb-122"><dt>**FVE \_ E \_ \_ enlazado \_ a un volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="726bb-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="726bb-123">Los protectores de clave no se pueden eliminar porque se está usando uno de ellos para desbloquear automáticamente el volumen.</span><span class="sxs-lookup"><span data-stu-id="726bb-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="726bb-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para deshabilitar el desbloqueo automático antes de ejecutar este método.</span><span class="sxs-lookup"><span data-stu-id="726bb-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="726bb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="726bb-125">Remarks</span></span>

<span data-ttu-id="726bb-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="726bb-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="726bb-127">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="726bb-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="726bb-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="726bb-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="726bb-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="726bb-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="726bb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726bb-130">Requirements</span></span>



| <span data-ttu-id="726bb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="726bb-131">Requirement</span></span> | <span data-ttu-id="726bb-132">Value</span><span class="sxs-lookup"><span data-stu-id="726bb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="726bb-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="726bb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="726bb-134">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="726bb-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="726bb-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="726bb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="726bb-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="726bb-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="726bb-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="726bb-137">Namespace</span></span><br/>                | <span data-ttu-id="726bb-138">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="726bb-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="726bb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="726bb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="726bb-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="726bb-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726bb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="726bb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726bb-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="726bb-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
