---
description: Windows Installer puede utilizar firmas digitales para detectar recursos dañados.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Firmas digitales y archivos. cab externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910957"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Firmas digitales y archivos. cab externos

Windows Installer puede utilizar firmas digitales para detectar recursos dañados. Al instalar un recurso externo, el certificado de firmante que pertenece al recurso se puede comprobar con un certificado de firma de referencia creado en el paquete. El instalador no puede comprobar las firmas de los archivadores internos. Solo puede comprobar firmas digitales mediante la [tabla MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows Installer hace lo siguiente al instalar un archivo almacenado en un archivo. cab externo:

-   El instalador comprueba si la entrada de medios para ese contenedor externo aparece en la [tabla MsiDigitalSignature](msidigitalsignature-table.md). Un archivo almacenado en un archivo. cab externo se identifica con una entrada en la columna Cabinet de la [tabla de medios](media-table.md) que no tiene el prefijo " \# ".
-   Antes de abrir el archivo. cab externo, el instalador llama a WinVerifyTrust para extraer la información del certificado y hash actual. Si hay una discrepancia entre la información de firma actual del archivo. cab y la información de firma creada en el paquete, se produce un error en la instalación. Se produce un error en la instalación porque es posible que el archivo. cab se haya puesto en peligro y no sea de confianza.

Para obtener más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte la sección [seguridad](https://msdn.microsoft.com/library/cc527452.aspx) del kit de desarrollo de software (SDK) de Microsoft Windows.

Para obtener más información, vea [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate Table](msidigitalcertificate-table.md)y [MsiDigitalSignature Table](msidigitalsignature-table.md).

 

 
