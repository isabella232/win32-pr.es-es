---
description: Windows El instalador puede usar firmas digitales como medio para detectar recursos dañados.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1dbe8366093418e74ed4ab1cb8e8c23fb8036eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071885"
---
# <a name="msicertexe"></a>Msicert.exe

Windows El instalador puede usar firmas digitales como medio para detectar recursos dañados. Se puede comparar un certificado de firmante con el certificado de firmante de un recurso externo que va a instalar el paquete. Para obtener más información, [vea Firmas digitales y Windows Instalador](digital-signatures-and-windows-installer.md).

MsiCert.exe es una utilidad de línea de comandos que se puede usar para rellenar la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md) con la información de firma digital de un archivo contenedor externo. El archivo de archivador debe estar firmado digitalmente y debe aparecer en la [tabla Multimedia](media-table.md). MsiCert.exe usa la información del certificado de firmante del contenedor firmado digitalmente y creará y agregará las tablas MsiDigitalSignature y MsiDigitalCertificate a la base de datos si aún no existen.

## <a name="syntax"></a>Sintaxis

**msicert -d** *{database}* **-m** *{entrada multimedia}* **-c** *{archivador}* **\[ -h \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Las opciones de línea de comandos no tienen en cuenta las mayúsculas y minúsculas y se pueden usar delimitadores de barra diagonal en lugar de un guión.



| Opción | Parámetro        | Descripción                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | &lt;database&gt; | Base de datos (.msi archivo) que se está actualizando.                                                         |
| -M     | <media Id> | Entrada en el campo DiskId de la [tabla Media](media-table.md) en el registro del archivo de archivador. |
| -c     | &lt;Gabinete&gt;  | Ruta de acceso al archivo de archivador firmado digitalmente.                                                          |
| -H     |                  | Incluya el hash de la firma digital. Esta información es opcional.                                            |



 

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



