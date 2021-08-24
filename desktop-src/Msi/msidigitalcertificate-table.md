---
description: La tabla MsiDigitalCertificate almacena los certificados en formato de secuencia binaria y asocia cada certificado a una clave principal.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabla MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828785"
---
# <a name="msidigitalcertificate-table"></a>Tabla MsiDigitalCertificate

La tabla MsiDigitalCertificate almacena los certificados en formato de secuencia binaria y asocia cada certificado a una clave principal. La clave principal se usa para compartir certificados entre varios objetos firmados digitalmente. Un certificado digital es una credencial que proporciona un medio para comprobar la identidad. Para más información, consulte [Certificados digitales en](../seccrypto/digital-certificates.md) la sección [Criptografía](../seccrypto/cryptography-portal.md) del Kit de desarrollo de software (SDK) de Microsoft Windows Software.

Las [tablas MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate están disponibles a partir de Windows Installer versión 2.0.

Windows El instalador puede usar firmas digitales como medio para detectar recursos dañados. Windows La versión 2.0 del instalador solo puede comprobar las firmas digitales de los gabinetes externos y solo mediante el uso de las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y MsiDigitalCertificate.

A partir de Windows Installer versión 3.0, el instalador de Windows puede comprobar las firmas digitales de las revisiones (archivos .msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate. Para obtener más información, vea [Directrices para crear](guidelines-for-authoring-secure-installations.md) instalaciones seguras y aplicación de revisiones de control de cuentas de usuario [(UAC).](user-account-control--uac--patching.md)

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

Representación binaria del certificado digital. La columna CertData contiene la matriz de bytes codificada de un contexto de certificado. Este es el **miembro pbCertEncoded** de la [**estructura CERT \_ CONTEXT.**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) El contexto del certificado se puede obtener llamando a [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un archivo .cer.

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

[Instalador de firmas digitales Windows datos](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
