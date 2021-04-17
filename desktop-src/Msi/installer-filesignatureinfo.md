---
description: El método FileSignatureInfo del objeto Installer toma la ruta de acceso a un archivo y devuelve una matriz SAFEARRAY de bytes que representan el hash o el certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Instalador. FileSignatureInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653335"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="983c7-103">Instalador. FileSignatureInfo (método)</span><span class="sxs-lookup"><span data-stu-id="983c7-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="983c7-104">El método **FileSignatureInfo** del objeto [**Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve una matriz SafeArray de bytes que representan el hash o el certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="983c7-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="983c7-105">Los valores se pueden usar para rellenar las tablas [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="983c7-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="983c7-106">Para obtener más información, vea el [**tipo de datos SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="983c7-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="983c7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="983c7-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="983c7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="983c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983c7-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="983c7-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="983c7-110">Ruta de acceso completa a un archivo firmado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="983c7-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="983c7-111">Al rellenar las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* apunta a un archivo. CAB firmado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="983c7-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="983c7-112">Al rellenar las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate, *filePath* apunta a una revisión firmada digitalmente.</span><span class="sxs-lookup"><span data-stu-id="983c7-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="983c7-113">*Opciones*</span><span class="sxs-lookup"><span data-stu-id="983c7-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="983c7-114">Marcas de caso de error especiales.</span><span class="sxs-lookup"><span data-stu-id="983c7-114">Special error case flags.</span></span>



| <span data-ttu-id="983c7-115">Marca</span><span class="sxs-lookup"><span data-stu-id="983c7-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="983c7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="983c7-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="983c7-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="983c7-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="983c7-118">Con *Options* establecido en MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** siempre devuelve un error irrecuperable para un hash no válido.</span><span class="sxs-lookup"><span data-stu-id="983c7-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="983c7-119">Si *Options* no se establece en MsiSignatureOptionInvalidHashFatal y *Format* se establece en msiSignatureInfoCertificate, **FileSignatureInfo** no devuelve un error para un hash no válido.</span><span class="sxs-lookup"><span data-stu-id="983c7-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="983c7-120">*Format*</span><span class="sxs-lookup"><span data-stu-id="983c7-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="983c7-121">Información de firma solicitada.</span><span class="sxs-lookup"><span data-stu-id="983c7-121">The requested signature information.</span></span>



| <span data-ttu-id="983c7-122">Marca</span><span class="sxs-lookup"><span data-stu-id="983c7-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="983c7-123">Significado</span><span class="sxs-lookup"><span data-stu-id="983c7-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="983c7-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="983c7-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="983c7-125">Devuelve una matriz SAFEARRAY de bytes que representan el certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="983c7-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="983c7-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="983c7-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="983c7-127">Devuelve una matriz SAFEARRAY de bytes que representa el hash.</span><span class="sxs-lookup"><span data-stu-id="983c7-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983c7-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="983c7-128">Return value</span></span>

<span data-ttu-id="983c7-129">Si es correcto, el método devuelve una [matriz SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contienen el hash o el certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="983c7-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="983c7-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="983c7-130">Remarks</span></span>

<span data-ttu-id="983c7-131">Para crear una instalación firmada completamente comprobada mediante la automatización, use el método **FileSignatureInfo** para rellenar las tablas [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalSignature](msidigitalsignature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="983c7-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="983c7-132">Para obtener más información, vea [crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="983c7-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="983c7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="983c7-133">Requirements</span></span>



| <span data-ttu-id="983c7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="983c7-134">Requirement</span></span> | <span data-ttu-id="983c7-135">Value</span><span class="sxs-lookup"><span data-stu-id="983c7-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983c7-136">Versión</span><span class="sxs-lookup"><span data-stu-id="983c7-136">Version</span></span><br/> | <span data-ttu-id="983c7-137">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="983c7-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="983c7-138">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="983c7-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="983c7-139">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="983c7-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="983c7-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="983c7-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="983c7-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="983c7-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="983c7-142">IID</span><span class="sxs-lookup"><span data-stu-id="983c7-142">IID</span></span><br/>     | <span data-ttu-id="983c7-143">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="983c7-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="983c7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="983c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983c7-145">Crear una instalación firmada completamente comprobada mediante automatización</span><span class="sxs-lookup"><span data-stu-id="983c7-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="983c7-146">Firmas digitales y Windows Installer</span><span class="sxs-lookup"><span data-stu-id="983c7-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="983c7-147">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="983c7-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
