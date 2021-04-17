---
description: Devuelve la versión de metadatos de FVE del volumen.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Método GetVersion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686644"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e2f38-103">Método GetVersion de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="e2f38-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e2f38-104">El método **GetVersion** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) devuelve la versión de metadatos de FVE del volumen.</span><span class="sxs-lookup"><span data-stu-id="e2f38-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2f38-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="e2f38-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f38-107">*Versión* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e2f38-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f38-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2f38-108">Type: **uint32**</span></span>

<span data-ttu-id="e2f38-109">Entero sin signo que indica la versión de metadatos del volumen.</span><span class="sxs-lookup"><span data-stu-id="e2f38-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="e2f38-110">Value</span><span class="sxs-lookup"><span data-stu-id="e2f38-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="e2f38-111">Significado</span><span class="sxs-lookup"><span data-stu-id="e2f38-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e2f38-112"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e2f38-113">Se desconoce el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e2f38-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="e2f38-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="e2f38-115">Formato de Windows Vista, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2f38-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="e2f38-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="e2f38-117">Formato de Windows 7, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows 7 o que el formato de metadatos se actualizó mediante el método [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="e2f38-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f38-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f38-118">Return value</span></span>

<span data-ttu-id="e2f38-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2f38-119">Type: **uint32**</span></span>

<span data-ttu-id="e2f38-120">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="e2f38-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="e2f38-121">Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e2f38-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="e2f38-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f38-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e2f38-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2f38-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="e2f38-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="e2f38-125">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e2f38-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="e2f38-126"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="e2f38-127">El valor del parámetro *version* no es válido.</span><span class="sxs-lookup"><span data-stu-id="e2f38-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e2f38-128"><dt>**Error \_ de \_Datos no válidos**</dt> <dt>(0xd)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="e2f38-129">El controlador devolvió un formato de datos no admitido.</span><span class="sxs-lookup"><span data-stu-id="e2f38-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e2f38-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2f38-130">Remarks</span></span>

<span data-ttu-id="e2f38-131">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e2f38-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2f38-132">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e2f38-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e2f38-133">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e2f38-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2f38-134">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e2f38-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f38-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f38-135">Requirements</span></span>



| <span data-ttu-id="e2f38-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f38-136">Requirement</span></span> | <span data-ttu-id="e2f38-137">Value</span><span class="sxs-lookup"><span data-stu-id="e2f38-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f38-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f38-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f38-139">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2f38-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2f38-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f38-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f38-141">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2f38-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2f38-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2f38-142">Namespace</span></span><br/>                | <span data-ttu-id="e2f38-143">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="e2f38-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e2f38-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e2f38-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2f38-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2f38-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f38-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2f38-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f38-147">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="e2f38-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
