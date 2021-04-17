---
description: Devuelve la clave externa de un archivo.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Método GetExternalKeyFromFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688163"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="961c6-103">Método GetExternalKeyFromFile de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="961c6-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="961c6-104">El método **GetExternalKeyFromFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la clave externa de un archivo creado por [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dada la ubicación de ese archivo.</span><span class="sxs-lookup"><span data-stu-id="961c6-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="961c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="961c6-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="961c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="961c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961c6-107">*PathWithFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="961c6-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961c6-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="961c6-108">Type: **string**</span></span>

<span data-ttu-id="961c6-109">Cadena que especifica la ubicación del archivo que contiene una clave externa.</span><span class="sxs-lookup"><span data-stu-id="961c6-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="961c6-110">*ExternalKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="961c6-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961c6-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="961c6-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="961c6-112">Matriz de bytes que es la clave externa de 256 bits incluida en el archivo que se puede usar para desbloquear un volumen.</span><span class="sxs-lookup"><span data-stu-id="961c6-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961c6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="961c6-113">Return value</span></span>

<span data-ttu-id="961c6-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="961c6-114">Type: **uint32**</span></span>

<span data-ttu-id="961c6-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="961c6-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="961c6-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="961c6-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="961c6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="961c6-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="961c6-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="961c6-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="961c6-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="961c6-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="961c6-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="961c6-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="961c6-121">El archivo no contiene una clave externa.</span><span class="sxs-lookup"><span data-stu-id="961c6-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="961c6-122"><dt>**Error \_ de \_No \_ se encontró el archivo**</dt> <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="961c6-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="961c6-123">No se encuentra el archivo en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="961c6-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="961c6-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="961c6-124">Remarks</span></span>

<span data-ttu-id="961c6-125">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="961c6-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="961c6-126">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="961c6-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="961c6-127">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="961c6-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="961c6-128">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="961c6-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="961c6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="961c6-129">Requirements</span></span>



| <span data-ttu-id="961c6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="961c6-130">Requirement</span></span> | <span data-ttu-id="961c6-131">Value</span><span class="sxs-lookup"><span data-stu-id="961c6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961c6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="961c6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="961c6-133">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="961c6-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="961c6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="961c6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="961c6-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="961c6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="961c6-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="961c6-136">Namespace</span></span><br/>                | <span data-ttu-id="961c6-137">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="961c6-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="961c6-138">MOF</span><span class="sxs-lookup"><span data-stu-id="961c6-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="961c6-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="961c6-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="961c6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="961c6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961c6-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="961c6-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
