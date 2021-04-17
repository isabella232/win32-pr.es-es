---
description: Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279340"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados. Un certificado de firmante puede compararse con el certificado de firma de un recurso externo que debe instalar el paquete. Para obtener más información, consulte [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe es una utilidad de línea de comandos que se puede usar para rellenar la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md) con la información de la firma digital de un archivo. cab externo. El archivo. cab debe firmarse digitalmente y mostrarse en la [tabla de medios](media-table.md). MsiCert.exe usa la información del certificado del firmante del archivo. CAB firmado digitalmente y creará y agregará las tablas MsiDigitalSignature y MsiDigitalCertificate a la base de datos, si aún no existen.

## <a name="syntax"></a>Sintaxis

**msicert-d** *{Database}* **-m** *{media entry}* **-c** *{Cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Las opciones de la línea de comandos no distinguen mayúsculas de minúsculas y se pueden usar delimitadores de barra diagonal en lugar de un guión.



| Opción | Parámetro        | Descripción                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | La base de datos (archivo. msi) que se está actualizando.                                                         |
| -M     | <media Id> | La entrada en el campo de despatín de la [tabla de medios](media-table.md) en el registro del archivo. cab. |
| -c     | <cabinet>  | La ruta de acceso al archivo. CAB firmado digitalmente.                                                          |
| -H     |                  | Incluye el hash de la firma digital. Esto es opcional.                                            |



 

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



