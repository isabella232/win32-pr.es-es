---
description: Para ayudar a mantener un entorno seguro durante la instalación del software, siga estas instrucciones al crear el paquete de Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Directrices para crear instalaciones seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d18e66c38480149ddad9e381c6461ffe50cf0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652829"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Directrices para crear instalaciones seguras

El cumplimiento de las siguientes directrices al crear un paquete de Windows Installer ayuda a mantener un entorno seguro durante la instalación:

-   Los administradores deben instalar las aplicaciones administradas en una carpeta de instalación de destino para la que los usuarios que no sean administradores no tengan privilegios de cambio o modificación.
-   Convierta cualquier propiedad establecida por el usuario en una propiedad pública. Los usuarios que interactúan con la interfaz de usuario no pueden cambiar las propiedades privadas. Para obtener información, consulte [acerca de las propiedades](about-properties.md).
-   No use propiedades para contraseñas u otra información que deba permanecer segura. El instalador puede escribir el valor de una propiedad creada en la [tabla de propiedades](property-table.md), o bien crearse en tiempo de ejecución, en un registro o en el registro del sistema. Para obtener más información, consulte [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Cuando la instalación requiere que el instalador use privilegios [*elevados*](e-gly.md) , use [las propiedades públicas restringidas](restricted-public-properties.md) para restringir las propiedades públicas que un usuario puede cambiar. Normalmente, algunas restricciones son necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios *elevados* .
-   Evite la instalación de servicios que suplanten los privilegios de un usuario determinado, ya que esto puede escribir datos de seguridad en un registro o en el registro del sistema. Esto crea posibles problemas de seguridad, conflictos de contraseñas o la pérdida de datos de configuración cuando se reinicia el sistema. Para obtener más información, consulte [tabla ServiceInstall](serviceinstall-table.md).
-   Use la tabla [LockPermissions](lockpermissions-table.md) y la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) para proteger servicios, archivos, claves del registro y carpetas creadas en un entorno bloqueado.
-   Agregue una firma digital a la instalación para asegurar la integridad de los archivos. Para obtener más información, consulte [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y [crear una instalación firmada completamente comprobada](authoring-a-fully-verified-signed-installation.md).
-   Cree el paquete de Windows Installer de modo que, si se deniega el acceso a los recursos, el programa de instalación produce un error de forma que mantiene un entorno seguro. Compruebe los privilegios de acceso del usuario y determine si hay suficiente espacio en disco antes de comenzar la instalación. Normalmente, el instalador solo debe mostrar un cuadro de diálogo examinar si el usuario actual es un administrador o si la instalación no requiere privilegios [*elevados*](e-gly.md) . Para obtener más información, consulte [resistencia de origen](source-resiliency.md).
-   Use [transformaciones seguras](secured-transforms.md) para almacenar transformaciones en un sistema de archivos seguro localmente en el equipo del usuario. Esto evita que el usuario tenga acceso de escritura a la transformación.
-   Para obtener información sobre cómo proteger los orígenes multimedia de las aplicaciones administradas, consulte [resistencia de origen](source-resiliency.md).
-   Use la propiedad [**Resumen de seguridad**](security-summary.md) para indicar si el paquete debe abrirse como de solo lectura. Esta propiedad debe establecerse en solo lectura como recomendado para una base de datos de instalación y en la aplicación de solo lectura para una transformación o revisión.
-   De forma predeterminada, el instalador ejecuta acciones personalizadas con privilegios de usuario para limitar el acceso de las acciones personalizadas al sistema. El instalador puede ejecutar acciones personalizadas con privilegios [*elevados*](e-gly.md) si se instala una aplicación administrada o si se ha especificado la Directiva del sistema para privilegios elevados. Para obtener más información, vea seguridad de la [acción personalizada](custom-action-security.md).
-   Use la directiva [DisablePatch](disablepatch.md) para proporcionar seguridad en entornos en los que se debe restringir la revisión.
-   Use la [tabla AppID](appid-table.md) para registrar los valores de configuración y seguridad comunes para los objetos DCOM.
-   Para obtener información relacionada, consulte [directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md).
-   Para obtener información relacionada, consulte [directrices para proteger paquetes en equipos bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md).
-   A partir de Windows Installer 3,0, la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores revisar las aplicaciones instaladas en el contexto por equipo. La revisión de UAC se habilita proporcionando un certificado de firmante en la tabla [MsiPatchCertificate](msipatchcertificate-table.md) y firmando las revisiones con el mismo certificado.
-   La capacidad del Windows Installer 5,0 para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del registro puede ayudar a que las aplicaciones de instalación sean más seguras. Para obtener más información, consulte [protección de recursos](securing-resources-.md).

 

 



