---
description: Usa la cadena de identificador de seguridad (SID) Active Directory proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Método UnlockWithAdSid de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668475"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4abb4-103">Método UnlockWithAdSid de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="4abb4-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4abb4-104">El método **UnlockWithAdSid** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la cadena de identificador de seguridad (SID) Active Directory proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="4abb4-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="4abb4-105">Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="4abb4-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4abb4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4abb4-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="4abb4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4abb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abb4-108">*SidString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4abb4-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abb4-109">Cadena que contiene el Active Directory SID.</span><span class="sxs-lookup"><span data-stu-id="4abb4-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abb4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4abb4-110">Return value</span></span>

<span data-ttu-id="4abb4-111">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4abb4-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4abb4-112">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4abb4-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4abb4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4abb4-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4abb4-114"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="4abb4-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4abb4-115">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4abb4-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4abb4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4abb4-116">Remarks</span></span>

<span data-ttu-id="4abb4-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4abb4-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4abb4-118">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4abb4-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4abb4-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4abb4-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4abb4-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4abb4-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4abb4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4abb4-121">Requirements</span></span>



| <span data-ttu-id="4abb4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4abb4-122">Requirement</span></span> | <span data-ttu-id="4abb4-123">Value</span><span class="sxs-lookup"><span data-stu-id="4abb4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abb4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4abb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4abb4-125">Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="4abb4-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4abb4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4abb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4abb4-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4abb4-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4abb4-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4abb4-128">Namespace</span></span><br/>                | <span data-ttu-id="4abb4-129">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="4abb4-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4abb4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4abb4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4abb4-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4abb4-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abb4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4abb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abb4-133">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4abb4-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
