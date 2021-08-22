---
description: Windows El instalador puede usar firmas digitales para detectar recursos dañados.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Firmas digitales y archivos de gabinete externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40edd8527eb93a6b970b3a8ce18fec8cc81f4688804a4e18f7ec5cdd748f3eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947469"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Firmas digitales y archivos de gabinete externos

Windows El instalador puede usar firmas digitales para detectar recursos dañados. Al instalar un recurso externo, el certificado de firmante que pertenece al recurso se puede comprobar con un certificado de firmante de referencia que se ha escrito en el paquete. El instalador no puede comprobar las firmas de los gabinetes internos. Solo puede comprobar las firmas digitales mediante la [tabla MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows El instalador hace lo siguiente al instalar un archivo almacenado en un gabinete externo:

-   El instalador comprueba si la entrada multimedia de ese contenedor externo aparece en la [tabla MsiDigitalSignature](msidigitalsignature-table.md). Un archivo almacenado en un gabinete externo se identifica teniendo [](media-table.md) una entrada en la columna Gabinete de la tabla Multimedia que no está precedida por un carácter \# ' '.
-   Antes de abrir el gabinete externo, el instalador llama a WinVerifyTrust para extraer el certificado actual y la información de hash. Si hay una discrepancia entre la información de firma actual en el archivador y la información de firma que se crea en el paquete, se produce un error en la instalación. Se produce un error en la instalación porque el gabinete puede estar en peligro y no puede ser de confianza.

Para más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust,**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)consulte la sección Seguridad del Kit de desarrollo de software (SDK) de Microsoft Windows. [](https://msdn.microsoft.com/library/cc527452.aspx)

Para obtener más información, [**vea MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md)y [MsiDigitalSignature table](msidigitalsignature-table.md).

 

 
