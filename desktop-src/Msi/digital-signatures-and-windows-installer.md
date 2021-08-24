---
description: El Windows puede usar firmas digitales para detectar recursos dañados.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Firma digital e instalador de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692815"
---
# <a name="digital-signatures-and-windows-installer"></a>Firma digital e instalador de Windows

El Windows puede usar firmas digitales para detectar recursos dañados. Un certificado de firmante se puede comparar con el certificado de firmante de un recurso externo que va a instalar el paquete. Para más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust,**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)consulte la sección Seguridad del Kit de desarrollo de software (SDK) de Microsoft Windows. [](https://msdn.microsoft.com/library/cc527452.aspx)

Con Windows Installer, las firmas digitales se pueden usar con paquetes de Windows Installer, transformaciones, revisiones, módulos de combinación y archivos de archivado externos. Windows El instalador se integra con la directiva de restricción de software en Microsoft Windows XP. Se pueden crear directivas para permitir o evitar instalaciones basadas en distintos criterios, incluido un publicador o certificado de firmante determinado. El Windows puede realizar la validación de firmas de archivos de gabinete externos en todas las plataformas en las que está instalada la versión 2.0 de CryptoAPI.

Tenga en cuenta que el ejemplo Setup.exe arranque proporcionado con el SDK del instalador de Windows realiza una comprobación de firma en un paquete del instalador de Windows antes de iniciar la instalación.

Al realizar [una instalación administrativa,](administrative-installation.md) se quita la firma digital del paquete. Una instalación administrativa modifica el paquete de instalación para agregar el flujo AdminProperties, lo que invalidaría la firma digital original. Un administrador puede volver asign el paquete.

Al aplicar una revisión a una instalación administrativa también se quita la firma digital del paquete. El motivo es que los cambios persisten en el paquete de instalación con revisión de la instalación administrativa. Un administrador puede volver asign el paquete.

A partir de Windows Installer versión 3.0, la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores aplicar revisiones a las aplicaciones instaladas en el contexto por equipo. La aplicación de revisiones de UAC se habilita proporcionando un certificado de firmante en la tabla [MsiPatchCertificate](msipatchcertificate-table.md) y firmando revisiones con el mismo certificado.

Para obtener más información, vea [Firmas digitales](digital-signatures-and-external-cabinet-files.md)y archivos de gabinete externos , instalador de Windows y directiva de restricción de [software](windows-installer-and-software-restriction-policy.md) [,](authoring-a-fully-verified-signed-installation.md)Creación de una instalación firmada totalmente verificada y Una dirección URL basada en Windows ejemplo de instalación del [instalador](a-url-based-windows-installer-installation-example.md).

 

 
