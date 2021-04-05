---
description: La tabla MsiDigitalCertificate almacena los certificados en formato de flujo binario y asocia cada certificado con una clave principal.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabla MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812710"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="74be3-103">Tabla MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="74be3-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="74be3-104">La tabla MsiDigitalCertificate almacena los certificados en formato de flujo binario y asocia cada certificado con una clave principal.</span><span class="sxs-lookup"><span data-stu-id="74be3-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="74be3-105">La clave principal se utiliza para compartir certificados entre varios objetos firmados digitalmente.</span><span class="sxs-lookup"><span data-stu-id="74be3-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="74be3-106">Un certificado digital es una credencial que proporciona un medio para comprobar la identidad.</span><span class="sxs-lookup"><span data-stu-id="74be3-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="74be3-107">Para obtener más información, vea [certificados digitales](../seccrypto/digital-certificates.md) en la sección [Criptografía](../seccrypto/cryptography-portal.md) del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="74be3-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="74be3-108">Las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate están disponibles a partir de Windows Installer versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="74be3-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="74be3-109">Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados.</span><span class="sxs-lookup"><span data-stu-id="74be3-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="74be3-110">Windows Installer versión 2,0 solo puede comprobar las firmas digitales de los archivadores externos y solo mediante el uso de las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="74be3-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="74be3-111">A partir de Windows Installer versión 3,0, el Windows Installer puede comprobar las firmas digitales de las revisiones (archivos. msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="74be3-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="74be3-112">Para obtener más información, consulte [directrices para la creación de instalaciones seguras](guidelines-for-authoring-secure-installations.md) y la [revisión del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="74be3-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="74be3-113">La tabla MsiDigitalCertificate tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="74be3-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="74be3-114">Columna</span><span class="sxs-lookup"><span data-stu-id="74be3-114">Column</span></span>             | <span data-ttu-id="74be3-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="74be3-115">Type</span></span>                         | <span data-ttu-id="74be3-116">Clave</span><span class="sxs-lookup"><span data-stu-id="74be3-116">Key</span></span> | <span data-ttu-id="74be3-117">Nullable</span><span class="sxs-lookup"><span data-stu-id="74be3-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="74be3-118">DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="74be3-118">DigitalCertificate</span></span> | [<span data-ttu-id="74be3-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="74be3-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="74be3-120">Y</span><span class="sxs-lookup"><span data-stu-id="74be3-120">Y</span></span>   | <span data-ttu-id="74be3-121">N</span><span class="sxs-lookup"><span data-stu-id="74be3-121">N</span></span>        |
| <span data-ttu-id="74be3-122">CertData</span><span class="sxs-lookup"><span data-stu-id="74be3-122">CertData</span></span>           | [<span data-ttu-id="74be3-123">Binario</span><span class="sxs-lookup"><span data-stu-id="74be3-123">Binary</span></span>](binary.md)         | <span data-ttu-id="74be3-124">N</span><span class="sxs-lookup"><span data-stu-id="74be3-124">N</span></span>   | <span data-ttu-id="74be3-125">N</span><span class="sxs-lookup"><span data-stu-id="74be3-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="74be3-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="74be3-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="74be3-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="74be3-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="74be3-128">Identifica el certificado de firma digital.</span><span class="sxs-lookup"><span data-stu-id="74be3-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="74be3-129">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="74be3-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="74be3-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span><span class="sxs-lookup"><span data-stu-id="74be3-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="74be3-131">Representación binaria del certificado digital.</span><span class="sxs-lookup"><span data-stu-id="74be3-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="74be3-132">La columna CertData contiene la matriz de bytes codificada de un contexto de certificado.</span><span class="sxs-lookup"><span data-stu-id="74be3-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="74be3-133">Este es el miembro **pbCertEncoded** de la estructura de [**\_ contexto CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="74be3-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="74be3-134">El contexto de certificado se puede obtener llamando a [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un archivo. cer.</span><span class="sxs-lookup"><span data-stu-id="74be3-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="74be3-135">Validación</span><span class="sxs-lookup"><span data-stu-id="74be3-135">Validation</span></span>

<dl>

[<span data-ttu-id="74be3-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="74be3-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="74be3-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="74be3-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="74be3-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="74be3-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="74be3-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="74be3-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="74be3-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="74be3-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="74be3-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="74be3-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="74be3-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74be3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74be3-143">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="74be3-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="74be3-144">Tabla MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="74be3-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="74be3-145">Firmas digitales y Windows Installer</span><span class="sxs-lookup"><span data-stu-id="74be3-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
