---
description: Crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Método PrepareVolume de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154062"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d4938-103">Método PrepareVolume de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d4938-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d4938-104">El método **PrepareVolume** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección.</span><span class="sxs-lookup"><span data-stu-id="d4938-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="d4938-105">Se debe llamar a este método antes de que se pueda proteger el volumen con cualquiera de los métodos \**ProtectKeyWith \** _.</span><span class="sxs-lookup"><span data-stu-id="d4938-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4938-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4938-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="d4938-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4938-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4938-108">_DiscoveryVolumeType \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d4938-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4938-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d4938-109">Type: **string**</span></span>

<span data-ttu-id="d4938-110">Cadena que especifica el tipo de volumen de detección.</span><span class="sxs-lookup"><span data-stu-id="d4938-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="d4938-111">Value</span><span class="sxs-lookup"><span data-stu-id="d4938-111">Value</span></span>               | <span data-ttu-id="d4938-112">Significado</span><span class="sxs-lookup"><span data-stu-id="d4938-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d4938-113">**&lt;ninguna&gt;**</span><span class="sxs-lookup"><span data-stu-id="d4938-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="d4938-114">No hay ningún volumen de detección.</span><span class="sxs-lookup"><span data-stu-id="d4938-114">No discovery volume.</span></span> <span data-ttu-id="d4938-115">Este valor crea un volumen de BitLocker nativo.</span><span class="sxs-lookup"><span data-stu-id="d4938-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="d4938-116">**&lt;predeterminada&gt;**</span><span class="sxs-lookup"><span data-stu-id="d4938-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="d4938-117">Este valor es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d4938-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="d4938-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="d4938-118">**FAT32**</span></span>           | <span data-ttu-id="d4938-119">Este valor crea un volumen de detección FAT32.</span><span class="sxs-lookup"><span data-stu-id="d4938-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="d4938-120">*ForceEncryptionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4938-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4938-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4938-121">Type: **uint32**</span></span>

<span data-ttu-id="d4938-122">Entero que especifica el tipo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d4938-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="d4938-123">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d4938-123">This can be one of the following values.</span></span>

| <span data-ttu-id="d4938-124">Value</span><span class="sxs-lookup"><span data-stu-id="d4938-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="d4938-125">Significado</span><span class="sxs-lookup"><span data-stu-id="d4938-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="d4938-126">No <dt>**especificado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d4938-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="d4938-127">No se ha especificado el tipo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d4938-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="d4938-128"><dt>**Software**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d4938-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="d4938-129">Cifrado de software.</span><span class="sxs-lookup"><span data-stu-id="d4938-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="d4938-130"><dt>**Hardware**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4938-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="d4938-131">Cifrado de hardware.</span><span class="sxs-lookup"><span data-stu-id="d4938-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4938-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4938-132">Return value</span></span>

<span data-ttu-id="d4938-133">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4938-133">Type: **uint32**</span></span>

<span data-ttu-id="d4938-134">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d4938-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="d4938-135">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4938-135">Return code/value</span></span>      | <span data-ttu-id="d4938-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4938-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="d4938-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="d4938-137">**S_OK**</span></span> <br/> <span data-ttu-id="d4938-138">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d4938-138">0 (0x0)</span></span> | <span data-ttu-id="d4938-139">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4938-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="d4938-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4938-140">Remarks</span></span>

<span data-ttu-id="d4938-141">Si no llama a este método al habilitar un volumen de BitLocker, es lo mismo que llamar a este método con el valor predeterminado en el parámetro *DiscoveryVolumeType* .</span><span class="sxs-lookup"><span data-stu-id="d4938-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4938-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4938-142">Requirements</span></span>

| <span data-ttu-id="d4938-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4938-143">Requirement</span></span> | <span data-ttu-id="d4938-144">Value</span><span class="sxs-lookup"><span data-stu-id="d4938-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4938-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4938-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d4938-146">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4938-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4938-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4938-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d4938-148">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4938-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d4938-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4938-149">Namespace</span></span><br/>                | <span data-ttu-id="d4938-150">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d4938-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d4938-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d4938-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4938-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4938-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d4938-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4938-153">See also</span></span>

[<span data-ttu-id="d4938-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d4938-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
