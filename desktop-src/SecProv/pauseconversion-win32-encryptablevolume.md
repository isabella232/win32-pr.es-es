---
description: Pausa el cifrado o descifrado de un volumen.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Método PauseConversion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688016"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="906c2-103">Método PauseConversion de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="906c2-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="906c2-104">El método **PauseConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) pausa el cifrado o descifrado de un volumen.</span><span class="sxs-lookup"><span data-stu-id="906c2-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="906c2-105">Si el disco es compatible con el cifrado de hardware, esta función puede pausar una operación de eliminación, pero no puede pausar el cifrado basado en hardware.</span><span class="sxs-lookup"><span data-stu-id="906c2-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="906c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="906c2-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="906c2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="906c2-107">Parameters</span></span>

<span data-ttu-id="906c2-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="906c2-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="906c2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="906c2-109">Return value</span></span>

<span data-ttu-id="906c2-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="906c2-110">Type: **uint32**</span></span>

<span data-ttu-id="906c2-111">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="906c2-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="906c2-112">Si este método se usa en un volumen totalmente cifrado o completamente descifrado, o si el cifrado o descifrado ya está pausado en el volumen, se devuelve 0 si no se produce ningún otro error.</span><span class="sxs-lookup"><span data-stu-id="906c2-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="906c2-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="906c2-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="906c2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="906c2-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="906c2-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="906c2-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="906c2-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="906c2-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="906c2-117"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="906c2-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="906c2-118">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="906c2-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="906c2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="906c2-119">Remarks</span></span>

<span data-ttu-id="906c2-120">Si este método se usa en un volumen con cifrado o descifrado en curso, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en pausa.</span><span class="sxs-lookup"><span data-stu-id="906c2-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="906c2-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="906c2-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="906c2-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="906c2-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="906c2-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="906c2-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="906c2-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="906c2-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="906c2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="906c2-125">Requirements</span></span>



| <span data-ttu-id="906c2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="906c2-126">Requirement</span></span> | <span data-ttu-id="906c2-127">Value</span><span class="sxs-lookup"><span data-stu-id="906c2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="906c2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="906c2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="906c2-129">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="906c2-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="906c2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="906c2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="906c2-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="906c2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="906c2-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="906c2-132">Namespace</span></span><br/>                | <span data-ttu-id="906c2-133">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="906c2-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="906c2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="906c2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="906c2-135"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="906c2-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="906c2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="906c2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906c2-137">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="906c2-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
