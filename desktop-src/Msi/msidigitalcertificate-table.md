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
# <a name="msidigitalcertificate-table"></a>Tabla MsiDigitalCertificate

La tabla MsiDigitalCertificate almacena los certificados en formato de flujo binario y asocia cada certificado con una clave principal. La clave principal se utiliza para compartir certificados entre varios objetos firmados digitalmente. Un certificado digital es una credencial que proporciona un medio para comprobar la identidad. Para obtener más información, vea [certificados digitales](../seccrypto/digital-certificates.md) en la sección [Criptografía](../seccrypto/cryptography-portal.md) del kit de desarrollo de software (SDK) de Microsoft Windows.

Las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate están disponibles a partir de Windows Installer versión 2,0.

Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados. Windows Installer versión 2,0 solo puede comprobar las firmas digitales de los archivadores externos y solo mediante el uso de las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate.

A partir de Windows Installer versión 3,0, el Windows Installer puede comprobar las firmas digitales de las revisiones (archivos. msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate. Para obtener más información, consulte [directrices para la creación de instalaciones seguras](guidelines-for-authoring-secure-installations.md) y la [revisión del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).

La tabla MsiDigitalCertificate tiene las columnas siguientes.



| Columna             | Tipo                         | Clave | Nullable |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [Identificador](identifier.md) | Y   | N        |
| CertData           | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Identifica el certificado de firma digital. Clave principal de la tabla.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

Representación binaria del certificado digital. La columna CertData contiene la matriz de bytes codificada de un contexto de certificado. Este es el miembro **pbCertEncoded** de la estructura de [**\_ contexto CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) . El contexto de certificado se puede obtener llamando a [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un archivo. cer.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Tabla MsiDigitalSignature](msidigitalsignature-table.md)
</dt> <dt>

[Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
