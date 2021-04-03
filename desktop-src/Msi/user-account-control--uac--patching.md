---
description: La aplicación de revisiones de control de cuentas de usuario (UAC) permite a los autores de instalaciones Windows Installer identificar revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Revisión de control de cuentas de usuario (UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913450"
---
# <a name="user-account-control-uac-patching"></a>Revisión de control de cuentas de usuario (UAC)

La aplicación de revisiones de [*control de cuentas de usuario*](u-gly.md) (UAC) permite a los autores de instalaciones Windows Installer identificar revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.

Si la firma digital no coincide con el certificado, Windows Vista muestra un cuadro de diálogo de UAC que solicita autorización de administrador antes de instalar la revisión. En sistemas anteriores a Windows Vista, el instalador no aplicará una revisión firmada que no coincida con el certificado.

Si un usuario no administrador intenta aplicar una revisión a una aplicación y no se cumplen las siguientes condiciones, Windows Vista notificará al usuario que se necesita autorización de administrador antes de instalar la revisión. Un usuario que no sea administrador puede seguir instalando la revisión sin necesidad de obtener autorización de administrador adicional, siempre que se cumplan las siguientes condiciones.

-   La aplicación se instaló en Windows Vista o Windows XP con Windows Installer 3,0 o posterior.

    **Windows Server 2008:** No compatible.

-   Si la aplicación se instaló en Windows XP, la aplicación también se debe haber instalado desde un medio extraíble, como un disco de CD-ROM o DVD. Esta restricción no se aplica si la aplicación se instaló en Windows Vista.
-   La aplicación no se instaló desde una imagen de origen de [instalación administrativa](administrative-installation.md) .
-   La aplicación se instaló originalmente por equipo. Para obtener información acerca de cómo permitir que los usuarios que no son administradores apliquen revisiones a aplicaciones administradas por el usuario después de que un administrador haya aprobado la revisión como de confianza, consulte [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md).
-   La [tabla MsiPatchCertificate](msipatchcertificate-table.md) se encuentra en el paquete del instalador de Windows (archivo. msi) y contiene la información necesaria para habilitar UAC. Es posible que la tabla y la información se hayan incluido en el paquete de instalación original o que se hayan agregado al paquete mediante un archivo de revisión de Windows Installer (archivo. msp).
-   Las revisiones se firman digitalmente con un certificado que aparece en la [tabla MsiPatchCertificate](msipatchcertificate-table.md). Para obtener más información sobre los certificados de firma digital, consulte [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).
-   La firma digital del paquete de revisión se puede comprobar con el certificado de la [tabla MsiPatchCertificate](msipatchcertificate-table.md). Para obtener más información acerca del uso de firmas digitales, certificados digitales y [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), consulte la sección [seguridad](https://msdn.microsoft.com/library/cc527452.aspx) del kit de desarrollo de software (SDK) de Microsoft Windows.
-   El certificado de firmante que se usa para comprobar la firma digital en el paquete de revisión es válido y no se ha revocado.
    > [!Note]  
    > Aunque no puede firmar una revisión mediante un certificado expirado, la evaluación de una firma digital en una revisión no genera un error si el certificado ha expirado. La evaluación usa la [tabla MsiPatchCertificate](msipatchcertificate-table.md)actual, que consta de la tabla MsiPatchCertificate en el paquete original y los cambios realizados en la tabla por revisiones secuenciados antes de la actual. Una revisión puede agregar nuevos certificados a la tabla MsiPatchCertificate para evaluar las revisiones secuenciadas después de la revisión actual. Siempre se rechaza un certificado revocado.

     

-   La revisión con privilegios mínimos no se ha deshabilitado mediante el establecimiento de la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o de la directiva [DisableLUAPatching](disableluapatching.md) .

Una revisión que se ha aplicado mediante la aplicación de revisiones de UAC también puede quitarla un usuario que no sea de administrador.

Los administradores pueden aplicar revisiones a los productos instalados por equipo independientemente de la configuración de UAC de la aplicación.

Puede determinar si la aplicación de revisiones con privilegios mínimos está habilitada para una aplicación mediante la función [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para consultar la propiedad INSTALLPROPERTY de la \_ \_ aplicación Lua autorizada o mediante \_ el método [**ProductInfo**](installer-productinfo.md) para consultar la propiedad "AuthorizedLUAApp". Si el valor de cualquiera de las propiedades es 1, la aplicación se habilita para la revisión de la cuenta de usuario con privilegios mínimos.

Un administrador puede deshabilitar la revisión de privilegios mínimos en el equipo estableciendo la directiva [DisableLUAPatching](disableluapatching.md) en 1. Puede establecer la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) en 1 durante la instalación inicial de una aplicación para evitar la aplicación de revisiones con privilegios mínimos solo para esa aplicación.

Esta funcionalidad está disponible a partir de Windows Installer versión 3,0. La revisión del control de cuentas de usuario (UAC) se denominaba revisión de la cuenta de usuario con privilegios mínimos (LUA) en Windows XP. La revisión de LUA no está disponible en Windows 2000 y Windows Server 2003.

Para obtener más información acerca de la compatibilidad de aplicaciones y el desarrollo de aplicaciones compatibles con el control de cuentas de usuario (UAC), consulte la información de UAC que se proporciona en [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

 

 
