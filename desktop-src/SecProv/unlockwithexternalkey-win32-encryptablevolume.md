---
description: Usa una clave externa proporcionada para tener acceso al contenido de un volumen de datos.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668470"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="12c6d-103">Método UnlockWithExternalKey de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="12c6d-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="12c6d-104">El método **UnlockWithExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una clave externa proporcionada para tener acceso al contenido de un volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="12c6d-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="12c6d-105">La clave de cifrado del volumen debe estar protegida con uno o más protectores de clave del tipo "clave externa" mediante el método [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear el volumen con este método.</span><span class="sxs-lookup"><span data-stu-id="12c6d-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="12c6d-106">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="12c6d-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="12c6d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12c6d-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="12c6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12c6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c6d-109">*ExternalKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="12c6d-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c6d-110">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="12c6d-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="12c6d-111">Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="12c6d-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="12c6d-112">Esta clave se puede obtener llamando al método [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="12c6d-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c6d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12c6d-113">Return value</span></span>

<span data-ttu-id="12c6d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12c6d-114">Type: **uint32**</span></span>

<span data-ttu-id="12c6d-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="12c6d-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="12c6d-116">Si el volumen ya está desbloqueado, este método devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="12c6d-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="12c6d-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12c6d-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="12c6d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="12c6d-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12c6d-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="12c6d-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="12c6d-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="12c6d-121"><dt>**Error \_ de NO \_ se encontró**</dt> <dt>ningún valor dado (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="12c6d-122">El volumen no tiene un protector de clave del tipo "external key".</span><span class="sxs-lookup"><span data-stu-id="12c6d-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="12c6d-123"><dt>**Error \_ de \_Contraseña no válida**</dt> ; <dt>no se especificó ningún valor (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="12c6d-124">Uno o varios protectores de clave del tipo "clave externa" existen, pero el parámetro *ExternalKey* especificado no puede desbloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="12c6d-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="12c6d-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="12c6d-126">El parámetro *ExternalKey* no es una matriz de tamaño 4.</span><span class="sxs-lookup"><span data-stu-id="12c6d-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="12c6d-127"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="12c6d-128">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="12c6d-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="12c6d-129">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="12c6d-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="12c6d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12c6d-130">Remarks</span></span>

<span data-ttu-id="12c6d-131">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="12c6d-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="12c6d-132">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="12c6d-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="12c6d-133">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="12c6d-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="12c6d-134">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="12c6d-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c6d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c6d-135">Requirements</span></span>



| <span data-ttu-id="12c6d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c6d-136">Requirement</span></span> | <span data-ttu-id="12c6d-137">Value</span><span class="sxs-lookup"><span data-stu-id="12c6d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c6d-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12c6d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="12c6d-139">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="12c6d-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12c6d-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12c6d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="12c6d-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12c6d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12c6d-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12c6d-142">Namespace</span></span><br/>                | <span data-ttu-id="12c6d-143">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="12c6d-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="12c6d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="12c6d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12c6d-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12c6d-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c6d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="12c6d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c6d-147">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="12c6d-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
