---
description: Indica si el volumen se desbloquea automáticamente cuando se monta.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Método IsAutoUnlockEnabled de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686643"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="eeaa4-103">Método IsAutoUnlockEnabled de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="eeaa4-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="eeaa4-104">El método **IsAutoUnlockEnabled** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen se desbloquea automáticamente al montarlo (por ejemplo, cuando los dispositivos de memoria extraíbles están conectados al equipo).</span><span class="sxs-lookup"><span data-stu-id="eeaa4-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="eeaa4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeaa4-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="eeaa4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeaa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeaa4-107">*IsAutoUnlockEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eeaa4-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeaa4-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eeaa4-108">Type: **boolean**</span></span>

<span data-ttu-id="eeaa4-109">Valor booleano que es true si la clave externa usada para desbloquear automáticamente el volumen existe y se ha almacenado en el volumen del sistema operativo que se está ejecutando actualmente; en caso contrario, es false.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="eeaa4-110">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eeaa4-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeaa4-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="eeaa4-111">Type: **string**</span></span>

<span data-ttu-id="eeaa4-112">Un identificador de cadena único que contiene el identificador de protector de clave de volumen cifrado asociado si *IsAutoUnlockEnabled* es true.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="eeaa4-113">Si *IsAutoUnlockEnabled* es false, *VolumeKeyProtectorID* es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeaa4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeaa4-114">Return value</span></span>

<span data-ttu-id="eeaa4-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eeaa4-115">Type: **uint32**</span></span>

<span data-ttu-id="eeaa4-116">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="eeaa4-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeaa4-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="eeaa4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeaa4-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eeaa4-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="eeaa4-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="eeaa4-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="eeaa4-121"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="eeaa4-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="eeaa4-122">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="eeaa4-123">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="eeaa4-124"><dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="eeaa4-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="eeaa4-125">No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="eeaa4-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeaa4-126">Remarks</span></span>

<span data-ttu-id="eeaa4-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eeaa4-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eeaa4-128">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eeaa4-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eeaa4-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="eeaa4-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeaa4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeaa4-131">Requirements</span></span>



| <span data-ttu-id="eeaa4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeaa4-132">Requirement</span></span> | <span data-ttu-id="eeaa4-133">Value</span><span class="sxs-lookup"><span data-stu-id="eeaa4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeaa4-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeaa4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eeaa4-135">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="eeaa4-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eeaa4-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeaa4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eeaa4-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeaa4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eeaa4-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eeaa4-138">Namespace</span></span><br/>                | <span data-ttu-id="eeaa4-139">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="eeaa4-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="eeaa4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="eeaa4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeaa4-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeaa4-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeaa4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeaa4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeaa4-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="eeaa4-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
