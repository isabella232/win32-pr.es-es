---
description: El Windows Installer puede utilizar firmas digitales para detectar recursos dañados.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Firmas digitales y Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668131"
---
# <a name="digital-signatures-and-windows-installer"></a>Firmas digitales y Windows Installer

El Windows Installer puede utilizar firmas digitales para detectar recursos dañados. Un certificado de firmante puede compararse con el certificado de firma de un recurso externo que debe instalar el paquete. Para obtener más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte la sección [seguridad](https://msdn.microsoft.com/library/cc527452.aspx) del kit de desarrollo de software (SDK) de Microsoft Windows.

Con Windows Installer, se pueden usar firmas digitales con paquetes Windows Installer, transformaciones, revisiones, módulos de combinación y archivos. cab externos. Windows Installer se integra con la Directiva de restricción de software en Microsoft Windows XP. Las directivas se pueden crear para permitir o evitar instalaciones basadas en criterios diferentes, incluido un certificado o publicador de firma determinado. El Windows Installer puede realizar la validación de la firma de archivos contenedores externos en todas las plataformas en las que se instala la versión 2,0 de CryptoAPI.

Tenga en cuenta que el ejemplo Setup.exe bootstrap proporcionado con el SDK de Windows Installer realiza una comprobación de firma en un paquete de Windows Installer antes de iniciar la instalación.

Al realizar una [instalación administrativa](administrative-installation.md) , se quita la firma digital del paquete. Una instalación administrativa modifica el paquete de instalación con el fin de agregar la secuencia AdminProperties, que invalidaría la firma digital original. Un administrador puede volver a firmar el paquete.

Al aplicar una revisión a una instalación administrativa, también se quita la firma digital del paquete. La razón es que los cambios se conservan en el paquete de instalación revisado de la instalación administrativa. Un administrador puede volver a firmar el paquete.

A partir de Windows Installer versión 3,0, la aplicación de [revisiones de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores revisar las aplicaciones instaladas en el contexto por equipo. La revisión de UAC se habilita proporcionando un certificado de firmante en la tabla [MsiPatchCertificate](msipatchcertificate-table.md) y firmando las revisiones con el mismo certificado.

Para obtener más información, consulte [firmas digitales y archivos. cab externos](digital-signatures-and-external-cabinet-files.md), [Windows Installer y Directiva de restricción de software](windows-installer-and-software-restriction-policy.md), [crear una instalación firmada completamente comprobada](authoring-a-fully-verified-signed-installation.md)y [una dirección URL basada Windows Installer ejemplo de instalación](a-url-based-windows-installer-installation-example.md).

 

 
