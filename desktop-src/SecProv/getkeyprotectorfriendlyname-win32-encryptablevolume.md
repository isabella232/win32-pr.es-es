---
description: Recupera el nombre para mostrar usado para identificar un protector de clave determinado.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Método GetKeyProtectorFriendlyName de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688156"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4c02a-103">Método GetKeyProtectorFriendlyName de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="4c02a-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4c02a-104">El método **GetKeyProtectorFriendlyName** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el nombre para mostrar que se usa para identificar un protector de clave determinado.</span><span class="sxs-lookup"><span data-stu-id="4c02a-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c02a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c02a-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="4c02a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c02a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c02a-107">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c02a-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c02a-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="4c02a-108">Type: **string**</span></span>

<span data-ttu-id="4c02a-109">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="4c02a-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-110">*FriendlyName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4c02a-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c02a-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="4c02a-111">Type: **string**</span></span>

<span data-ttu-id="4c02a-112">Una cadena que contiene el nombre especificado por el usuario que se usa para identificar el protector de clave determinado.</span><span class="sxs-lookup"><span data-stu-id="4c02a-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c02a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c02a-113">Return value</span></span>

<span data-ttu-id="4c02a-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c02a-114">Type: **uint32**</span></span>

<span data-ttu-id="4c02a-115">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4c02a-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4c02a-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c02a-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="4c02a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c02a-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c02a-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="4c02a-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4c02a-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4c02a-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="4c02a-121">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave válido.</span><span class="sxs-lookup"><span data-stu-id="4c02a-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="4c02a-122"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="4c02a-123">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="4c02a-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4c02a-124">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4c02a-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c02a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c02a-125">Remarks</span></span>

<span data-ttu-id="4c02a-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4c02a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4c02a-127">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4c02a-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4c02a-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4c02a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4c02a-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c02a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c02a-130">Requirements</span></span>



| <span data-ttu-id="4c02a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c02a-131">Requirement</span></span> | <span data-ttu-id="4c02a-132">Value</span><span class="sxs-lookup"><span data-stu-id="4c02a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c02a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c02a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4c02a-134">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c02a-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4c02a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c02a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4c02a-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c02a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c02a-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c02a-137">Namespace</span></span><br/>                | <span data-ttu-id="4c02a-138">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="4c02a-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4c02a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4c02a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c02a-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c02a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c02a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c02a-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4c02a-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
