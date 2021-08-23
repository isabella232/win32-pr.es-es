---
description: Windows El instalador puede usar firmas digitales como medio para detectar recursos dañados.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede88930cdb6cc616d8c39fb400f0c67c31eecd01d6d1a7d1832421cb394bcc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534555"
---
# <a name="msicertexe"></a>Msicert.exe

Windows El instalador puede usar firmas digitales como medio para detectar recursos dañados. Se puede comparar un certificado de firmante con el certificado de firmante de un recurso externo que va a instalar el paquete. Para obtener más información, [vea Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe es una utilidad de línea de comandos que se puede usar para rellenar la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md) con la información de firma digital de un archivo contenedor externo. El archivo de archivador debe estar firmado digitalmente y aparecer en la [tabla Media](media-table.md). MsiCert.exe la información del certificado de firmante del contenedor firmado digitalmente y creará y agregará las tablas MsiDigitalSignature y MsiDigitalCertificate a la base de datos si aún no existen.

## <a name="syntax"></a>Syntax

**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Las opciones de línea de comandos no tienen en cuenta mayúsculas de minúsculas y se pueden usar delimitadores de barra diagonal en lugar de un guion.



| Opción | Parámetro        | Descripción                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | Base de datos (.msi archivo) que se está actualizando.                                                         |
| -M     | <media Id> | Entrada en el campo DiskId de la [tabla Media](media-table.md) en el registro del archivo de archivador. |
| -c     | <cabinet>  | Ruta de acceso al archivo de archivador firmado digitalmente.                                                          |
| -H     |                  | Incluya el hash de la firma digital. Esta información es opcional.                                            |



 

Esta herramienta solo está disponible en los componentes Windows [SDK para desarrolladores Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



