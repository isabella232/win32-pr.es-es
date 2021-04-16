---
description: Determina si el volumen se encuentra en una unidad que admite o puede admitir el cifrado de hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Método GetHardwareEncryptionStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686652"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e60c8-103">Método GetHardwareEncryptionStatus de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="e60c8-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e60c8-104">El método **GetHardwareEncryptionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) determina si el volumen se encuentra en una unidad que admita o admita el cifrado de hardware.</span><span class="sxs-lookup"><span data-stu-id="e60c8-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e60c8-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e60c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e60c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e60c8-107">*HardwareEncryptionStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e60c8-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e60c8-108">Especifica si la unidad puede admitir el cifrado de hardware.</span><span class="sxs-lookup"><span data-stu-id="e60c8-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="e60c8-109">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e60c8-109">This can be one of the following values.</span></span>



| <span data-ttu-id="e60c8-110">Value</span><span class="sxs-lookup"><span data-stu-id="e60c8-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="e60c8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="e60c8-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="e60c8-112"><dt>**No compatible**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e60c8-113">No se admite el cifrado de hardware.</span><span class="sxs-lookup"><span data-stu-id="e60c8-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="e60c8-114"><dt>**Sin protección**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e60c8-115">No se admite el cifrado de unidad.</span><span class="sxs-lookup"><span data-stu-id="e60c8-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="e60c8-116"><dt>**Utiliza el software**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e60c8-117">El método de cifrado está basado en software.</span><span class="sxs-lookup"><span data-stu-id="e60c8-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="e60c8-118"><dt>**Usa hardware**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e60c8-119">La unidad admite el cifrado de hardware.</span><span class="sxs-lookup"><span data-stu-id="e60c8-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e60c8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e60c8-120">Return value</span></span>

<span data-ttu-id="e60c8-121">Esta función devuelve cero (0) si el volumen es compatible con el cifrado de hardware de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e60c8-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="e60c8-122">De lo contrario, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="e60c8-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="e60c8-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e60c8-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="e60c8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e60c8-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e60c8-125"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e60c8-126">El volumen es compatible con el cifrado de hardware de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e60c8-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e60c8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e60c8-127">Requirements</span></span>



| <span data-ttu-id="e60c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e60c8-128">Requirement</span></span> | <span data-ttu-id="e60c8-129">Value</span><span class="sxs-lookup"><span data-stu-id="e60c8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e60c8-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e60c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e60c8-131">Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="e60c8-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e60c8-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e60c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e60c8-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e60c8-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e60c8-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e60c8-134">Namespace</span></span><br/>                | <span data-ttu-id="e60c8-135">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="e60c8-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e60c8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e60c8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e60c8-137"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60c8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e60c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60c8-139">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="e60c8-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




