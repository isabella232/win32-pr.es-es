---
description: Realiza una copia de seguridad de los datos de recuperación en Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Método BackupRecoveryInformationToActiveDirectory de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688666"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2c644-103">Método BackupRecoveryInformationToActiveDirectory de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="2c644-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2c644-104">El método **BackupRecoveryInformationToActiveDirectory** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) realiza copias de seguridad de los datos de recuperación en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c644-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="2c644-105">Este método requiere que haya un protector de contraseña numérica en el volumen.</span><span class="sxs-lookup"><span data-stu-id="2c644-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="2c644-106">También se debe configurar directiva de grupo para habilitar la copia de seguridad de la información de recuperación en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c644-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c644-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c644-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="2c644-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c644-109">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c644-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c644-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="2c644-110">Type: **string**</span></span>

<span data-ttu-id="2c644-111">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="2c644-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="2c644-112">Este protector de clave debe ser un protector de contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="2c644-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c644-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c644-113">Return value</span></span>

<span data-ttu-id="2c644-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c644-114">Type: **uint32**</span></span>

<span data-ttu-id="2c644-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2c644-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2c644-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c644-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="2c644-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c644-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c644-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="2c644-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="2c644-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c644-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="2c644-120"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2c644-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="2c644-121">Directiva de grupo no permite el almacenamiento de la información de recuperación en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c644-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="2c644-122"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2c644-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="2c644-123">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="2c644-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2c644-124">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2c644-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="2c644-125"><dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido</span><span class="sxs-lookup"><span data-stu-id="2c644-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="2c644-126">El protector de clave especificado no es un protector de clave numérico.</span><span class="sxs-lookup"><span data-stu-id="2c644-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="2c644-127">Debe especificar un protector de contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="2c644-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="2c644-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c644-128">Requirements</span></span>



| <span data-ttu-id="2c644-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c644-129">Requirement</span></span> | <span data-ttu-id="2c644-130">Value</span><span class="sxs-lookup"><span data-stu-id="2c644-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c644-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c644-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c644-132">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c644-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2c644-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c644-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c644-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c644-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c644-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c644-135">Namespace</span></span><br/>                | <span data-ttu-id="2c644-136">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="2c644-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2c644-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2c644-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c644-138"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c644-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c644-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c644-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c644-140">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="2c644-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




