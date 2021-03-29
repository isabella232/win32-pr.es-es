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
# <a name="msidigitalsignature-table"></a>Tabla MsiDigitalSignature

La tabla MsiDigitalSignature contiene la información de firma para todos los objetos firmados digitalmente en la base de datos de instalación.

Las tablas MsiDigitalSignature y [MsiDigitalCertificate](msidigitalcertificate-table.md) están disponibles a partir de Windows Installer versión 2,0.

Windows Installer versión puede utilizar firmas digitales como medio para detectar recursos dañados. Windows Installer 2,0 solo puede comprobar las firmas digitales de los archivadores externos y solo mediante el uso de las tablas MsiDigitalSignature y [MsiDigitalCertificate](msidigitalcertificate-table.md) .

A partir de Windows Installer 3,0, el Windows Installer puede comprobar las firmas digitales de revisiones (archivos. msp) mediante las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate. Para obtener más información, consulte [directrices para la creación de instalaciones seguras](guidelines-for-authoring-secure-installations.md) y la [revisión del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md).

La tabla MsiDigitalSignature tiene las columnas siguientes.



| Columna               | Tipo                         | Clave | Nullable |
|----------------------|------------------------------|-----|----------|
| Tabla                | [Identificador](identifier.md) | Y   | N        |
| SignObject           | [Texto](text.md)             | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |
| Hash                 | [Binario](binary.md)         | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Con la Windows Installer versión 2,0, la entrada de este campo debe ser "media" para la [tabla de medios](media-table.md). El instalador solo comprueba las firmas digitales en entradas de medios de archivo. cab externos. Esta columna y la columna SignObject especifican conjuntamente el recurso que está firmado digitalmente.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

Una clave externa en la clave principal de la tabla especificada por la columna de la tabla. Esta columna y la columna de la tabla especifican el recurso que está firmado digitalmente.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Una clave externa en la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md). Esto identifica el certificado que debe existir en el archivo para que la acción asociada se lleve a cabo correctamente. El recurso (u objeto) siempre es necesario para que coincida con este certificado en la tabla MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>LM
</dt> <dd>

En este campo, escriba el hash de referencia del recurso (u objeto) que se va a comprobar con el hash real del recurso (u objeto) obtenido en tiempo de ejecución. Si solo es necesario comprobar el certificado, el campo hash puede ser null. Tenga en cuenta que el formato del hash depende del tipo de recurso (u objeto) que se está firmando.

La columna hash contiene la representación binaria del hash. El contenido real es el miembro **pbData** de la estructura de [**\_ \_ blobs de hash de cifrado**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , que forma parte de la estructura de **\_ blobs CryptoAPI** . Esto se puede obtener llamando a [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) o a [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).

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

[Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
