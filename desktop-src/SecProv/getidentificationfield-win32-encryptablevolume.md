---
description: Devuelve la cadena de identificador disponible en los metadatos del volumen.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Método GetIdentificationField de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154064"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b84a6-103">Método GetIdentificationField de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="b84a6-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b84a6-104">El método **GetIdentificationField** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la cadena de identificador disponible en los metadatos del volumen.</span><span class="sxs-lookup"><span data-stu-id="b84a6-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b84a6-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="b84a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b84a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84a6-107">*IdentificationField* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b84a6-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b84a6-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="b84a6-108">Type: **string**</span></span>

<span data-ttu-id="b84a6-109">Cadena que especifica el campo de identificación que se asigna al volumen.</span><span class="sxs-lookup"><span data-stu-id="b84a6-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84a6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b84a6-110">Return value</span></span>

<span data-ttu-id="b84a6-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b84a6-111">Type: **uint32**</span></span>

<span data-ttu-id="b84a6-112">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b84a6-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b84a6-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b84a6-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b84a6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b84a6-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b84a6-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="b84a6-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b84a6-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b84a6-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="b84a6-117"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b84a6-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="b84a6-118">Esta unidad está bloqueada por Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b84a6-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="b84a6-119">Debe desbloquear este volumen en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="b84a6-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="b84a6-120"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b84a6-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="b84a6-121">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="b84a6-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b84a6-122">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b84a6-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="b84a6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b84a6-123">Requirements</span></span>



| <span data-ttu-id="b84a6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84a6-124">Requirement</span></span> | <span data-ttu-id="b84a6-125">Value</span><span class="sxs-lookup"><span data-stu-id="b84a6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84a6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b84a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b84a6-127">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="b84a6-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b84a6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b84a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b84a6-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b84a6-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b84a6-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b84a6-130">Namespace</span></span><br/>                | <span data-ttu-id="b84a6-131">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="b84a6-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b84a6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b84a6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b84a6-133"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b84a6-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b84a6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b84a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84a6-135">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b84a6-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




