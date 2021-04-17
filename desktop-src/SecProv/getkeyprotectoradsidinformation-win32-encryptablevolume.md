---
description: Recupera el identificador de seguridad y las marcas utilizadas para proteger una clave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Método GetKeyProtectorAdSidInformation de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105691117"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c9a34-103">Método GetKeyProtectorAdSidInformation de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="c9a34-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c9a34-104">El método **GetKeyProtectorAdSidInformation** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el identificador de seguridad y las marcas utilizadas para proteger una clave.</span><span class="sxs-lookup"><span data-stu-id="c9a34-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9a34-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c9a34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9a34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a34-107">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9a34-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a34-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="c9a34-108">Type: **string**</span></span>

<span data-ttu-id="c9a34-109">Identificador de cadena que se puede usar para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="c9a34-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="c9a34-110">*SidString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9a34-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a34-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="c9a34-111">Type: **string**</span></span>

<span data-ttu-id="c9a34-112">Cadena que contiene el identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="c9a34-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="c9a34-113">*Marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9a34-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a34-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a34-114">Type: **uint32**</span></span>

<span data-ttu-id="c9a34-115">Marcas que cambian el comportamiento de la función.</span><span class="sxs-lookup"><span data-stu-id="c9a34-115">Flags that change the function behavior.</span></span> <span data-ttu-id="c9a34-116">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9a34-116">This can be one of the following values.</span></span>



| <span data-ttu-id="c9a34-117">Value</span><span class="sxs-lookup"><span data-stu-id="c9a34-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="c9a34-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c9a34-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="c9a34-119"><dt>**FVE \_ Marca de DPAPI \_ ng \_ \_ ninguno**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="c9a34-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="c9a34-120">Ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="c9a34-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="c9a34-121"><dt>**FVE \_ \_ \_ Desbloqueo de la marca de DPAPI ng \_ \_ como \_ \_ cuenta de servicio**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c9a34-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c9a34-122">Especifica que el protector basado en SID se protegió en una cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="c9a34-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="c9a34-123">Si se especifica esta marca, el llamador debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (por ejemplo, mediante la eliminación temporal de la suplantación).</span><span class="sxs-lookup"><span data-stu-id="c9a34-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a34-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9a34-124">Return value</span></span>

<span data-ttu-id="c9a34-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a34-125">Type: **uint32**</span></span>

<span data-ttu-id="c9a34-126">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c9a34-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c9a34-127">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9a34-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c9a34-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a34-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c9a34-129"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="c9a34-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c9a34-130">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c9a34-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9a34-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9a34-131">Remarks</span></span>

<span data-ttu-id="c9a34-132">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c9a34-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9a34-133">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c9a34-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c9a34-134">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c9a34-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9a34-135">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c9a34-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a34-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a34-136">Requirements</span></span>



| <span data-ttu-id="c9a34-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a34-137">Requirement</span></span> | <span data-ttu-id="c9a34-138">Value</span><span class="sxs-lookup"><span data-stu-id="c9a34-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a34-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a34-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a34-140">Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9a34-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9a34-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a34-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a34-142">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9a34-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9a34-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9a34-143">Namespace</span></span><br/>                | <span data-ttu-id="c9a34-144">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="c9a34-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c9a34-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c9a34-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9a34-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9a34-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a34-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9a34-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a34-148">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="c9a34-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
