---
description: Deshabilita o suspende todos los protectores de clave asociados a este volumen.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Método DisableKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687570"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f101e-103">Método DisableKeyProtectors de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="f101e-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f101e-104">El método **DisableKeyProtectors** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) deshabilita o suspende todos los protectores de clave asociados a este volumen.</span><span class="sxs-lookup"><span data-stu-id="f101e-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f101e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f101e-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="f101e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f101e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f101e-107">*DisableCount* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f101e-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f101e-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f101e-108">Type: **uint32**</span></span>

<span data-ttu-id="f101e-109">Entero que especifica el número de reinicios para los que se deshabilitarán los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="f101e-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="f101e-110">Este parámetro solo está disponible en los volúmenes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f101e-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f101e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f101e-111">Return value</span></span>

<span data-ttu-id="f101e-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f101e-112">Type: **uint32**</span></span>

<span data-ttu-id="f101e-113">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f101e-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f101e-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f101e-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f101e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f101e-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f101e-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f101e-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f101e-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="f101e-118"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f101e-119">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f101e-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="f101e-120">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="f101e-120">Security Considerations</span></span>

<span data-ttu-id="f101e-121">Este método expone la clave de cifrado del volumen sin cifrar en el disco duro, desactivando cualquier protección de volumen.</span><span class="sxs-lookup"><span data-stu-id="f101e-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="f101e-122">Se recomienda no tener ninguna contraseña o clave de cifrado en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="f101e-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="f101e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f101e-123">Remarks</span></span>

<span data-ttu-id="f101e-124">Se pueden agregar nuevos protectores de clave incluso cuando se deshabilitan o se suspenden los protectores de clave.</span><span class="sxs-lookup"><span data-stu-id="f101e-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="f101e-125">Estos protectores de clave permanecerán deshabilitados a menos que se llame a [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="f101e-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="f101e-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f101e-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f101e-127">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f101e-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f101e-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f101e-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f101e-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f101e-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f101e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f101e-130">Requirements</span></span>



| <span data-ttu-id="f101e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f101e-131">Requirement</span></span> | <span data-ttu-id="f101e-132">Value</span><span class="sxs-lookup"><span data-stu-id="f101e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f101e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f101e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f101e-134">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f101e-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f101e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f101e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f101e-136">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f101e-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f101e-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f101e-137">Namespace</span></span><br/>                | <span data-ttu-id="f101e-138">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="f101e-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f101e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f101e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f101e-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f101e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f101e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f101e-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f101e-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="f101e-143">**EnableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="f101e-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
