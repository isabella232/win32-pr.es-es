---
description: Reanuda el cifrado o descifrado de un volumen.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Método ResumeConversion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809277"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="36a57-103">Método ResumeConversion de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="36a57-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="36a57-104">El método **ResumeConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) reanuda el cifrado o descifrado de un volumen.</span><span class="sxs-lookup"><span data-stu-id="36a57-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="36a57-105">Si el disco es compatible con el cifrado de hardware, esta función solo puede reanudar una operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="36a57-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="36a57-106">Para obtener más información, vea [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="36a57-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="36a57-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a57-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="36a57-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36a57-108">Parameters</span></span>

<span data-ttu-id="36a57-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="36a57-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36a57-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36a57-110">Return value</span></span>

<span data-ttu-id="36a57-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a57-111">Type: **uint32**</span></span>

<span data-ttu-id="36a57-112">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="36a57-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="36a57-113">Si este método se usa en un volumen totalmente cifrado o completamente descifrado, o si el cifrado o descifrado ya está en curso en el volumen, se devuelve 0 si no se produce ningún otro error.</span><span class="sxs-lookup"><span data-stu-id="36a57-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="36a57-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36a57-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="36a57-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="36a57-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="36a57-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="36a57-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="36a57-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a57-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="36a57-118"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="36a57-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="36a57-119">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="36a57-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="36a57-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36a57-120">Remarks</span></span>

<span data-ttu-id="36a57-121">Si este método se usa en un volumen con cifrado o descifrado en pausa, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en curso.</span><span class="sxs-lookup"><span data-stu-id="36a57-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="36a57-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="36a57-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36a57-123">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="36a57-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="36a57-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="36a57-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36a57-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="36a57-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36a57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a57-126">Requirements</span></span>



| <span data-ttu-id="36a57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a57-127">Requirement</span></span> | <span data-ttu-id="36a57-128">Value</span><span class="sxs-lookup"><span data-stu-id="36a57-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a57-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a57-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36a57-130">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="36a57-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36a57-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a57-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36a57-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="36a57-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36a57-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36a57-133">Namespace</span></span><br/>                | <span data-ttu-id="36a57-134">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="36a57-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="36a57-135">MOF</span><span class="sxs-lookup"><span data-stu-id="36a57-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36a57-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36a57-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a57-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="36a57-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a57-138">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="36a57-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
