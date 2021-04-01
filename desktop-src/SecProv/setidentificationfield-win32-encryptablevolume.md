---
description: Establece la cadena de identificador especificada en los metadatos del volumen.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Método SetIdentificationField de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912809"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a226a-103">Método SetIdentificationField de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="a226a-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a226a-104">El método **SetIdentificationField** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) establece la cadena de identificador especificada en los metadatos del volumen.</span><span class="sxs-lookup"><span data-stu-id="a226a-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="a226a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a226a-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="a226a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a226a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a226a-107">*IdentificationField* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a226a-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a226a-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a226a-108">Type: **string**</span></span>

<span data-ttu-id="a226a-109">Cadena que especifica el campo de identificación que se asigna al volumen.</span><span class="sxs-lookup"><span data-stu-id="a226a-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="a226a-110">Si la cadena opcional no está presente, se usan los valores del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="a226a-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="a226a-111">Si la cadena está presente y no está vacía, se usa el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a226a-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="a226a-112">El parámetro *IdentificationField* no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a226a-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a226a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a226a-113">Return value</span></span>

<span data-ttu-id="a226a-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a226a-114">Type: **uint32**</span></span>

<span data-ttu-id="a226a-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a226a-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a226a-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a226a-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="a226a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a226a-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a226a-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="a226a-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="a226a-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a226a-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="a226a-120"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="a226a-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="a226a-121">Esta unidad está bloqueada por Cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a226a-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="a226a-122">Debe desbloquear este volumen en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="a226a-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="a226a-123"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="a226a-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="a226a-124">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="a226a-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="a226a-125">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a226a-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="a226a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a226a-126">Requirements</span></span>



| <span data-ttu-id="a226a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a226a-127">Requirement</span></span> | <span data-ttu-id="a226a-128">Value</span><span class="sxs-lookup"><span data-stu-id="a226a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a226a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a226a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a226a-130">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="a226a-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a226a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a226a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a226a-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a226a-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a226a-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a226a-133">Namespace</span></span><br/>                | <span data-ttu-id="a226a-134">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="a226a-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a226a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a226a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a226a-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a226a-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a226a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a226a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a226a-138">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="a226a-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




