---
description: La tabla MsiDigitalSignature contiene la información de firma de cada objeto firmado digitalmente en la base de datos de instalación.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabla MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071869"
---
# <a name="msidigitalsignature-table"></a>Tabla MsiDigitalSignature

La tabla MsiDigitalSignature contiene la información de firma de cada objeto firmado digitalmente en la base de datos de instalación.

Las tablas MsiDigitalSignature y [MsiDigitalCertificate](msidigitalcertificate-table.md) están disponibles a partir de Windows Installer versión 2.0.

Windows La versión del instalador puede usar firmas digitales como medio para detectar recursos dañados. Windows El instalador 2.0 solo puede comprobar las firmas digitales de los gabinetes externos y solo mediante el uso de las tablas MsiDigitalSignature y [MsiDigitalCertificate.](msidigitalcertificate-table.md)

A partir de Windows Installer 3.0, el instalador de Windows puede comprobar las firmas digitales de las revisiones (archivos .msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate. Para obtener más información, vea [Directrices para crear](guidelines-for-authoring-secure-installations.md) instalaciones seguras y aplicación de revisiones de control de cuentas de usuario [(UAC).](user-account-control--uac--patching.md)

La tabla MsiDigitalSignature tiene las siguientes columnas.



| Columna               | Tipo                         | Clave | Nullable |
|----------------------|------------------------------|-----|----------|
| Tabla                | [Identificador](identifier.md) | Y   | N        |
| SignObject           | [Texto](text.md)             | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |
| Hash                 | [Binario](binary.md)         | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Con la Windows installer versión 2.0, la entrada de este campo debe ser "Media" para la [tabla Media](media-table.md). El instalador solo comprueba las firmas digitales en entradas de medios externos del gabinete. Esta columna y la columna SignObject juntos especifican el recurso firmado digitalmente.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

Clave externa en la clave principal de la tabla especificada por la columna Tabla . Esta columna y la columna Tabla juntos especifican el recurso firmado digitalmente.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Clave externa en la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md). Esto identifica el certificado que debe existir en el archivo para que la acción asociada se pueda realizar correctamente. El recurso (u objeto) siempre es necesario para que coincida con este certificado en la tabla MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash
</dt> <dd>

En este campo, escriba el hash de referencia del recurso (u objeto) que se va a comprobar con el hash real del recurso (u objeto) obtenido en tiempo de ejecución. Si solo es necesario comprobar el certificado, el campo Hash puede ser NULL. Tenga en cuenta que el formato del hash depende del tipo del recurso (u objeto) que se está firmando.

La columna Hash contiene la representación binaria del hash. El contenido real es el **miembro pbData** de la estructura [**\_ CRYPT HASH \_ BLOB,**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) que forma parte de la **estructura CRYPTOAPI \_ BLOB.** Esto se puede obtener llamando a [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) o [**MsiGetFileSignatureInformation.**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)

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

[Tabla MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> <dt>

[Instalador de firmas digitales Windows datos](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
