---
description: Recupera la clave externa para un protector de clave determinado.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Método GetKeyProtectorExternalKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275321"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9a003-103">Método GetKeyProtectorExternalKey de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="9a003-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9a003-104">El método **GetKeyProtectorExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la clave externa para un protector de clave determinado del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="9a003-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="9a003-105">El identificador de protector de clave debe hacer referencia a un protector de clave de tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="9a003-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="9a003-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a003-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="9a003-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a003-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a003-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a003-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a003-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="9a003-109">Type: **string**</span></span>

<span data-ttu-id="9a003-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a003-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="9a003-111">*ExternalKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a003-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a003-112">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="9a003-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="9a003-113">Matriz de bytes que especifica la clave externa de 256 bits que se puede usar para desbloquear el volumen correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9a003-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a003-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a003-114">Return value</span></span>

<span data-ttu-id="9a003-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a003-115">Type: **uint32**</span></span>

<span data-ttu-id="9a003-116">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9a003-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9a003-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a003-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="9a003-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a003-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a003-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="9a003-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="9a003-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a003-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="9a003-121"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="9a003-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="9a003-122">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9a003-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="9a003-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="9a003-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="9a003-124">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="9a003-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="9a003-125"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9a003-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="9a003-126">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="9a003-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9a003-127">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9a003-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="9a003-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a003-128">Remarks</span></span>

<span data-ttu-id="9a003-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9a003-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a003-130">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9a003-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9a003-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9a003-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a003-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9a003-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a003-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a003-133">Requirements</span></span>



| <span data-ttu-id="9a003-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a003-134">Requirement</span></span> | <span data-ttu-id="9a003-135">Value</span><span class="sxs-lookup"><span data-stu-id="9a003-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a003-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a003-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a003-137">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a003-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9a003-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a003-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a003-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a003-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a003-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a003-140">Namespace</span></span><br/>                | <span data-ttu-id="9a003-141">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="9a003-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9a003-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9a003-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a003-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a003-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a003-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a003-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a003-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="9a003-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
