---
description: La aplicación de revisiones de Control de cuentas de usuario (UAC) permite a los autores de las instalaciones del instalador de Windows identificar las revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Revisión de Control de cuentas de usuario (UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074285"
---
# <a name="user-account-control-uac-patching"></a>Revisión de Control de cuentas de usuario (UAC)

[*La aplicación*](u-gly.md) de revisiones de Control de cuentas de usuario (UAC) permite a los autores de las instalaciones del instalador de Windows identificar las revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.

Si la firma digital no coincide con el certificado, Windows Vista muestra un cuadro de diálogo de UAC que solicita autorización de administrador antes de instalar la revisión. En sistemas anteriores a Windows Vista, el instalador no aplicará una revisión firmada que no coincida con el certificado.

Si un usuario que no es administrador intenta aplicar una revisión a una aplicación y no se cumplen las condiciones siguientes, Windows Vista notificará al usuario que se requiere autorización de administrador antes de instalar la revisión. Un usuario que no sea administrador puede seguir instalando la revisión, sin necesidad de obtener una autorización de administrador adicional, siempre que se cumplen las condiciones siguientes.

-   La aplicación se instaló en Windows Vista o Windows XP mediante Windows Installer 3.0 o posterior.

    **Windows Server 2008:** No se admite.

-   Si la aplicación se instaló en Windows XP, la aplicación también se debe haber instalado desde medios extraíbles, como un disco CD-ROM o DVD. Esta restricción no se aplica si la aplicación se instaló en Windows Vista.
-   La aplicación no se instaló desde una [imagen de origen de instalación](administrative-installation.md) administrativa.
-   La aplicación se instaló originalmente por máquina. Para obtener información sobre cómo permitir que los usuarios que no son administradores apliquen revisiones a aplicaciones administradas por usuario después de que un administrador haya aprobado la revisión como de confianza, consulte Aplicación de revisiones Per-User [aplicaciones](patching-per-user-managed-applications.md)administradas.
-   La [tabla MsiPatchCertificate](msipatchcertificate-table.md) está presente en el paquete del instalador de ventana (.msi archivo) y contiene la información necesaria para habilitar UAC. Es posible que la tabla y la información se hayan incluido en el paquete de instalación original o se hayan agregado al paquete mediante un archivo de revisión de Windows Installer (archivo .msp).
-   Las revisiones están firmadas digitalmente por un certificado que aparece en la [tabla MsiPatchCertificate](msipatchcertificate-table.md). Para obtener más información sobre los certificados de firma digital, vea [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).
-   La firma digital del paquete de revisión se puede comprobar con el certificado de la [tabla MsiPatchCertificate](msipatchcertificate-table.md). Para más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust,**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)consulte la sección Seguridad del Kit de desarrollo de software (SDK) de Microsoft Windows. [](https://msdn.microsoft.com/library/cc527452.aspx)
-   El certificado de firmante usado para comprobar que la firma digital en el paquete de revisión es válida y no se ha revocado.
    > [!Note]  
    > Aunque no se puede firmar una revisión con un certificado expirado, la evaluación de una firma digital en una revisión no producirá un error si el certificado ha expirado. La evaluación usa la tabla [MsiPatchCertificate](msipatchcertificate-table.md)actual, que consta de la tabla MsiPatchCertificate del paquete original y de los cambios realizados en la tabla mediante revisiones secuenciadas antes de la actual. Una revisión puede agregar nuevos certificados a la tabla MsiPatchCertificate para evaluar las revisiones secuenciadas después de la revisión actual. Siempre se rechaza un certificado revocado.

     

-   La aplicación de revisiones con privilegios mínimos no se ha deshabilitado estableciendo la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o la [directiva DisableLUAPatching.](disableluapatching.md)

Un usuario que no sea administrador también puede quitar una revisión que se haya aplicado mediante la aplicación de revisiones de UAC.

Los administradores pueden aplicar revisiones a los productos instalados por máquina, independientemente de la configuración de UAC de la aplicación.

Puede determinar si la aplicación de revisiones con privilegios mínimos está habilitada para una aplicación mediante la función [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para consultar la propiedad INSTALLPROPERTY AUTHORIZED LUA APP o mediante el método ProductInfo para consultar la propiedad \_ \_ \_ "AuthorizedLUAApp". [](installer-productinfo.md) Si el valor de cualquiera de las propiedades es 1, la aplicación está habilitada para la aplicación de revisiones de cuentas de usuario con privilegios mínimos.

Un administrador puede deshabilitar la aplicación de revisiones con privilegios mínimos en el equipo estableciendo [la directiva DisableLUAPatching](disableluapatching.md) en 1. Puede establecer la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) en 1 durante la instalación inicial de una aplicación para evitar solo la aplicación con privilegios mínimos.

Esta funcionalidad está disponible a partir de Windows Installer versión 3.0. La aplicación de revisiones de Control de cuentas de usuario (UAC) se denominaba aplicación de revisiones de cuentas de usuario con privilegios mínimos (LUA) Windows XP. La aplicación de revisiones de LUA no está disponible Windows 2000 y Windows Server 2003.

Para obtener más información sobre la compatibilidad de aplicaciones y el desarrollo de aplicaciones compatibles con el Control de cuentas de usuario (UAC), consulte la información de UAC que se proporciona en [Microsoft Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

 

 
