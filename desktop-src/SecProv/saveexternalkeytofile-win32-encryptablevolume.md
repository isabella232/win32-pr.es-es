---
description: Escribe la clave externa asociada al protector de clave de volumen especificado en un archivo del sistema, oculto de solo lectura, en la carpeta especificada.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Método SaveExternalKeyToFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667894"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7fb01-103">Método SaveExternalKeyToFile de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="7fb01-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7fb01-104">El método **SaveExternalKeyToFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) escribe la clave externa asociada al protector de clave de volumen especificado en un archivo de solo lectura del sistema, oculto y de solo lectura en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="7fb01-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="7fb01-105">Este método solo se aplica a los protectores de clave del tipo "clave externa" o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="7fb01-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb01-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fb01-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="7fb01-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fb01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb01-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb01-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb01-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="7fb01-109">Type: **string**</span></span>

<span data-ttu-id="7fb01-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="7fb01-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="7fb01-111">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb01-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb01-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="7fb01-112">Type: **string**</span></span>

<span data-ttu-id="7fb01-113">Una cadena que contiene el volumen o la ubicación de la carpeta donde se va a guardar la clave externa asociada al protector de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="7fb01-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="7fb01-114">Esta ruta de acceso no incluye el nombre del archivo, que es interno y puede cambiar de una versión a una versión.</span><span class="sxs-lookup"><span data-stu-id="7fb01-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="7fb01-115">Use **GetExternalKeyFileName** para obtener el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7fb01-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb01-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fb01-116">Return value</span></span>

<span data-ttu-id="7fb01-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fb01-117">Type: **uint32**</span></span>

<span data-ttu-id="7fb01-118">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7fb01-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7fb01-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fb01-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="7fb01-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fb01-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fb01-121"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="7fb01-122">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7fb01-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="7fb01-123"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="7fb01-124">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7fb01-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="7fb01-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="7fb01-126">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "clave externa" o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="7fb01-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="7fb01-127"><dt>**Error \_ de Ruta de acceso \_ no \_ encontrada**</dt> <dt>2147942403 (0x80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="7fb01-128">El parámetro *path* no hace referencia a una ubicación válida.</span><span class="sxs-lookup"><span data-stu-id="7fb01-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="7fb01-129">Asegúrese de que el nombre de archivo no se incluye en el parámetro *path* .</span><span class="sxs-lookup"><span data-stu-id="7fb01-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="7fb01-130"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="7fb01-131">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="7fb01-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7fb01-132">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7fb01-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="7fb01-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fb01-133">Remarks</span></span>

<span data-ttu-id="7fb01-134">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fb01-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fb01-135">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7fb01-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7fb01-136">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7fb01-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fb01-137">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7fb01-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb01-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fb01-138">Requirements</span></span>



| <span data-ttu-id="7fb01-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fb01-139">Requirement</span></span> | <span data-ttu-id="7fb01-140">Value</span><span class="sxs-lookup"><span data-stu-id="7fb01-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb01-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fb01-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7fb01-142">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fb01-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fb01-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fb01-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7fb01-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fb01-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fb01-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fb01-145">Namespace</span></span><br/>                | <span data-ttu-id="7fb01-146">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7fb01-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7fb01-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7fb01-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fb01-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fb01-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb01-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fb01-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb01-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="7fb01-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
