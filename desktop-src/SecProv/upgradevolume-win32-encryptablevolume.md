---
description: Actualiza un volumen del formato de Windows Vista al formato de Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Método UpgradeVolume de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001044"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="14f4d-103">Método UpgradeVolume de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="14f4d-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="14f4d-104">El método **UpgradeVolume** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) actualiza un volumen del formato de Windows Vista al formato de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14f4d-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="14f4d-105">Se trata de una operación no revertida.</span><span class="sxs-lookup"><span data-stu-id="14f4d-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f4d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14f4d-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="14f4d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14f4d-107">Parameters</span></span>

<span data-ttu-id="14f4d-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="14f4d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14f4d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14f4d-109">Return value</span></span>

<span data-ttu-id="14f4d-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14f4d-110">Type: **uint32**</span></span>

<span data-ttu-id="14f4d-111">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="14f4d-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="14f4d-112">Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="14f4d-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="14f4d-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14f4d-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="14f4d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="14f4d-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14f4d-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="14f4d-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="14f4d-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="14f4d-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="14f4d-117"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="14f4d-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="14f4d-118">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="14f4d-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="14f4d-119"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="14f4d-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="14f4d-120">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="14f4d-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="14f4d-121"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="14f4d-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="14f4d-122">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="14f4d-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="14f4d-123">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="14f4d-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="14f4d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14f4d-124">Remarks</span></span>

<span data-ttu-id="14f4d-125">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="14f4d-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="14f4d-126">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="14f4d-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="14f4d-127">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="14f4d-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="14f4d-128">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="14f4d-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14f4d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14f4d-129">Requirements</span></span>



| <span data-ttu-id="14f4d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f4d-130">Requirement</span></span> | <span data-ttu-id="14f4d-131">Value</span><span class="sxs-lookup"><span data-stu-id="14f4d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f4d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14f4d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="14f4d-133">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="14f4d-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14f4d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14f4d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="14f4d-135">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="14f4d-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="14f4d-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14f4d-136">Namespace</span></span><br/>                | <span data-ttu-id="14f4d-137">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="14f4d-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="14f4d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="14f4d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14f4d-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14f4d-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f4d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="14f4d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f4d-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="14f4d-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
