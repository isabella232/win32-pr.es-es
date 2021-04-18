---
description: Devuelve el nombre del archivo que contiene la clave externa.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Método GetExternalKeyFileName de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686657"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6071d-103">Método GetExternalKeyFileName de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="6071d-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6071d-104">El método **GetExternalKeyFileName** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve el nombre del archivo que contiene la clave externa, si esta clave externa se guarda en una ubicación de archivo mediante el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="6071d-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="6071d-105">Este método solo se aplica a los protectores de clave del tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="6071d-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="6071d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6071d-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="6071d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6071d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6071d-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6071d-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6071d-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="6071d-109">Type: **string**</span></span>

<span data-ttu-id="6071d-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="6071d-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="6071d-111">*Nombre de archivo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6071d-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6071d-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="6071d-112">Type: **string**</span></span>

<span data-ttu-id="6071d-113">Una cadena que especifica el nombre con la extensión, pero sin la ruta de acceso del archivo, del archivo que contiene la clave externa.</span><span class="sxs-lookup"><span data-stu-id="6071d-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6071d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6071d-114">Return value</span></span>

<span data-ttu-id="6071d-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6071d-115">Type: **uint32**</span></span>

<span data-ttu-id="6071d-116">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6071d-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6071d-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6071d-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6071d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6071d-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6071d-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6071d-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6071d-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="6071d-121"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="6071d-122">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="6071d-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="6071d-123"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6071d-124">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6071d-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="6071d-125"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="6071d-126">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="6071d-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6071d-127">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6071d-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="6071d-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6071d-128">Remarks</span></span>

<span data-ttu-id="6071d-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6071d-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6071d-130">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6071d-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6071d-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6071d-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6071d-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6071d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6071d-133">Requirements</span></span>



| <span data-ttu-id="6071d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6071d-134">Requirement</span></span> | <span data-ttu-id="6071d-135">Value</span><span class="sxs-lookup"><span data-stu-id="6071d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6071d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6071d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6071d-137">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="6071d-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6071d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6071d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6071d-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6071d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6071d-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6071d-140">Namespace</span></span><br/>                | <span data-ttu-id="6071d-141">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="6071d-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6071d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6071d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6071d-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6071d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6071d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6071d-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6071d-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="6071d-146">**SaveExternalKeyToFile**</span><span class="sxs-lookup"><span data-stu-id="6071d-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
