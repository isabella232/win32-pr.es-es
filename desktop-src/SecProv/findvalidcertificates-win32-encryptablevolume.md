---
description: Enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Método FindValidCertificates de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361050"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8b809-103">Método FindValidCertificates de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="8b809-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8b809-104">El método **FindValidCertificates** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="8b809-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="8b809-105">La lista devuelta solo contiene certificados con un [*identificador de objeto*](../secgloss/o-gly.md) (OID) válido.</span><span class="sxs-lookup"><span data-stu-id="8b809-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="8b809-106">El OID puede ser el valor predeterminado, o bien se puede especificar en el directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8b809-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b809-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b809-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="8b809-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b809-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b809-109">*CertificateThumbprint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8b809-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b809-110">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="8b809-110">Type: **string\[\]**</span></span>

<span data-ttu-id="8b809-111">Matriz de cadenas que contiene la lista de certificados válidos.</span><span class="sxs-lookup"><span data-stu-id="8b809-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b809-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b809-112">Return value</span></span>

<span data-ttu-id="8b809-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b809-113">Type: **uint32**</span></span>

<span data-ttu-id="8b809-114">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8b809-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8b809-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b809-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="8b809-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b809-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="8b809-117"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="8b809-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="8b809-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8b809-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="8b809-119"><dt>**FVE \_ E \_ no \_ válido \_ OID de BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="8b809-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="8b809-120">El OID de BitLocker disponible no es válido.</span><span class="sxs-lookup"><span data-stu-id="8b809-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b809-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b809-121">Requirements</span></span>



| <span data-ttu-id="8b809-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b809-122">Requirement</span></span> | <span data-ttu-id="8b809-123">Value</span><span class="sxs-lookup"><span data-stu-id="8b809-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b809-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b809-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8b809-125">Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="8b809-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8b809-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b809-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8b809-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b809-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b809-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b809-128">Namespace</span></span><br/>                | <span data-ttu-id="8b809-129">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="8b809-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8b809-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8b809-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b809-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b809-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b809-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b809-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b809-133">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="8b809-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
