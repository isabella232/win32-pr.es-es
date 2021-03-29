---
description: La tabla MsiDigitalSignature contiene la información de firma para todos los objetos firmados digitalmente en la base de datos de instalación.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabla MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652561"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="d06da-103">Tabla MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="d06da-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="d06da-104">La tabla MsiDigitalSignature contiene la información de firma para todos los objetos firmados digitalmente en la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="d06da-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="d06da-105">Las tablas MsiDigitalSignature y [MsiDigitalCertificate](msidigitalcertificate-table.md) están disponibles a partir de Windows Installer versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="d06da-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="d06da-106">Windows Installer versión puede utilizar firmas digitales como medio para detectar recursos dañados.</span><span class="sxs-lookup"><span data-stu-id="d06da-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="d06da-107">Windows Installer 2,0 solo puede comprobar las firmas digitales de los archivadores externos y solo mediante el uso de las tablas MsiDigitalSignature y [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d06da-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="d06da-108">A partir de Windows Installer 3,0, el Windows Installer puede comprobar las firmas digitales de revisiones (archivos. msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="d06da-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="d06da-109">Para obtener más información, consulte [directrices para la creación de instalaciones seguras](guidelines-for-authoring-secure-installations.md) y la [revisión del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="d06da-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="d06da-110">La tabla MsiDigitalSignature tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="d06da-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="d06da-111">Columna</span><span class="sxs-lookup"><span data-stu-id="d06da-111">Column</span></span>               | <span data-ttu-id="d06da-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="d06da-112">Type</span></span>                         | <span data-ttu-id="d06da-113">Clave</span><span class="sxs-lookup"><span data-stu-id="d06da-113">Key</span></span> | <span data-ttu-id="d06da-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="d06da-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="d06da-115">Tabla</span><span class="sxs-lookup"><span data-stu-id="d06da-115">Table</span></span>                | [<span data-ttu-id="d06da-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="d06da-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="d06da-117">Y</span><span class="sxs-lookup"><span data-stu-id="d06da-117">Y</span></span>   | <span data-ttu-id="d06da-118">N</span><span class="sxs-lookup"><span data-stu-id="d06da-118">N</span></span>        |
| <span data-ttu-id="d06da-119">SignObject</span><span class="sxs-lookup"><span data-stu-id="d06da-119">SignObject</span></span>           | [<span data-ttu-id="d06da-120">Texto</span><span class="sxs-lookup"><span data-stu-id="d06da-120">Text</span></span>](text.md)             | <span data-ttu-id="d06da-121">Y</span><span class="sxs-lookup"><span data-stu-id="d06da-121">Y</span></span>   | <span data-ttu-id="d06da-122">N</span><span class="sxs-lookup"><span data-stu-id="d06da-122">N</span></span>        |
| <span data-ttu-id="d06da-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="d06da-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="d06da-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="d06da-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="d06da-125">N</span><span class="sxs-lookup"><span data-stu-id="d06da-125">N</span></span>   | <span data-ttu-id="d06da-126">N</span><span class="sxs-lookup"><span data-stu-id="d06da-126">N</span></span>        |
| <span data-ttu-id="d06da-127">Hash</span><span class="sxs-lookup"><span data-stu-id="d06da-127">Hash</span></span>                 | [<span data-ttu-id="d06da-128">Binario</span><span class="sxs-lookup"><span data-stu-id="d06da-128">Binary</span></span>](binary.md)         | <span data-ttu-id="d06da-129">N</span><span class="sxs-lookup"><span data-stu-id="d06da-129">N</span></span>   | <span data-ttu-id="d06da-130">Y</span><span class="sxs-lookup"><span data-stu-id="d06da-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d06da-131">Columnas</span><span class="sxs-lookup"><span data-stu-id="d06da-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d06da-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="d06da-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="d06da-133">Con la Windows Installer versión 2,0, la entrada de este campo debe ser "media" para la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="d06da-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="d06da-134">El instalador solo comprueba las firmas digitales en entradas de medios de archivo. cab externos.</span><span class="sxs-lookup"><span data-stu-id="d06da-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="d06da-135">Esta columna y la columna SignObject especifican conjuntamente el recurso que está firmado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="d06da-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="d06da-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span><span class="sxs-lookup"><span data-stu-id="d06da-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="d06da-137">Una clave externa en la clave principal de la tabla especificada por la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d06da-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="d06da-138">Esta columna y la columna de la tabla especifican el recurso que está firmado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="d06da-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="d06da-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="d06da-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="d06da-140">Una clave externa en la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="d06da-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="d06da-141">Esto identifica el certificado que debe existir en el archivo para que la acción asociada se lleve a cabo correctamente.</span><span class="sxs-lookup"><span data-stu-id="d06da-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="d06da-142">El recurso (u objeto) siempre es necesario para que coincida con este certificado en la tabla MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="d06da-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="d06da-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>LM</span><span class="sxs-lookup"><span data-stu-id="d06da-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="d06da-144">En este campo, escriba el hash de referencia del recurso (u objeto) que se va a comprobar con el hash real del recurso (u objeto) obtenido en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d06da-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="d06da-145">Si solo es necesario comprobar el certificado, el campo hash puede ser null.</span><span class="sxs-lookup"><span data-stu-id="d06da-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="d06da-146">Tenga en cuenta que el formato del hash depende del tipo de recurso (u objeto) que se está firmando.</span><span class="sxs-lookup"><span data-stu-id="d06da-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="d06da-147">La columna hash contiene la representación binaria del hash.</span><span class="sxs-lookup"><span data-stu-id="d06da-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="d06da-148">El contenido real es el miembro **pbData** de la estructura de [**\_ \_ blobs de hash de cifrado**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , que forma parte de la estructura de **\_ blobs CryptoAPI** .</span><span class="sxs-lookup"><span data-stu-id="d06da-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="d06da-149">Esto se puede obtener llamando a [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) o a [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span><span class="sxs-lookup"><span data-stu-id="d06da-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d06da-150">Validación</span><span class="sxs-lookup"><span data-stu-id="d06da-150">Validation</span></span>

<dl>

[<span data-ttu-id="d06da-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="d06da-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d06da-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="d06da-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d06da-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="d06da-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="d06da-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="d06da-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d06da-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="d06da-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="d06da-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="d06da-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d06da-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d06da-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06da-158">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="d06da-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="d06da-159">Tabla MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="d06da-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="d06da-160">Firmas digitales y Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d06da-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
