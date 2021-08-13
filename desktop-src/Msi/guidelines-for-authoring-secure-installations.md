---
description: Para ayudar a mantener un entorno seguro durante la instalación de software, siga estas directrices al crear el paquete Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Directrices para crear instalaciones seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f796594fe665875f63751d0da4cac5bd7cde621e04b4d1d35585c74755dd719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635803"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Directrices para crear instalaciones seguras

El cumplimiento de las siguientes directrices al crear un paquete Windows Installer ayuda a mantener un entorno seguro durante la instalación:

-   Los administradores deben instalar aplicaciones administradas en una carpeta de instalación de destino para la que los usuarios que no son administradores no tengan privilegios de cambio o modificación.
-   Convertir cualquier propiedad establecida por el usuario en una propiedad pública. El usuario que interactúa con la interfaz de usuario no puede cambiar las propiedades privadas. Para obtener información, vea [Acerca de las propiedades](about-properties.md).
-   No use propiedades para contraseñas u otra información que deba permanecer segura. El instalador puede escribir el valor de una propiedad creada en la tabla [Property](property-table.md)o creada en tiempo de ejecución en un registro o en el registro del sistema. Para obtener más información, vea [Evitar que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Cuando la instalación requiera que el instalador [*use*](e-gly.md) privilegios elevados, use [Propiedades](restricted-public-properties.md) públicas restringidas para restringir las propiedades públicas que un usuario puede cambiar. Algunas restricciones son normalmente necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use *privilegios* elevados.
-   Evite instalar servicios que suplante los privilegios de un usuario determinado, ya que esto puede escribir datos de seguridad en un registro o en el registro del sistema. Esto crea un posible problema de seguridad, un conflicto de contraseñas o la pérdida de datos de configuración cuando se reinicia el sistema. Para obtener más información, [vea ServiceInstall table](serviceinstall-table.md).
-   Use la [tabla LockPermissions](lockpermissions-table.md) y la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) para proteger servicios, archivos, claves del Registro y carpetas creadas en un entorno bloqueado.
-   Agregue firmas digitales a la instalación para garantizar la integridad de los archivos. Para obtener más información, [vea Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) y [Authoring a Fully Verified Signed Installation](authoring-a-fully-verified-signed-installation.md).
-   Cree el Windows installer de forma que, si se deniega al usuario el acceso a los recursos, se produce un error en la instalación de una manera que mantiene un entorno seguro. Compruebe los privilegios de acceso del usuario y determine si hay suficiente espacio en disco antes de comenzar la instalación. Normalmente, el instalador solo debe mostrar un cuadro de diálogo examinar si el usuario actual es administrador o si la instalación no requiere [*privilegios*](e-gly.md) elevados. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md)
-   Use [transformaciones protegidas](secured-transforms.md) para almacenar las transformaciones en un sistema de archivos seguro localmente en el equipo del usuario. Esto evita que el usuario tenga acceso de escritura a la transformación.
-   Para obtener información sobre cómo proteger orígenes multimedia de aplicaciones administradas, vea [Resistencia de origen](source-resiliency.md).
-   Use la [**propiedad Resumen de**](security-summary.md) seguridad para indicar si el paquete debe abrirse como de solo lectura. Esta propiedad debe establecerse en la opción de solo lectura recomendada para una base de datos de instalación y en que se aplique de solo lectura para una transformación o revisión.
-   El instalador ejecuta acciones personalizadas con privilegios de usuario de forma predeterminada para limitar el acceso de acciones personalizadas al sistema. El instalador puede ejecutar [](e-gly.md) acciones personalizadas con privilegios elevados si se está instalando una aplicación administrada o si se ha especificado la directiva del sistema para privilegios elevados. Para obtener más información, vea [Seguridad de acciones personalizadas.](custom-action-security.md)
-   Use la [directiva DisablePatch](disablepatch.md) para proporcionar seguridad en entornos donde se debe restringir la aplicación de revisiones.
-   Use la [tabla AppId para](appid-table.md) registrar valores comunes de seguridad y configuración para objetos DCOM.
-   Para obtener información relacionada, vea [Directrices para proteger acciones personalizadas.](guidelines-for-securing-custom-actions.md)
-   Para obtener información relacionada, vea [Directrices para proteger paquetes en equipos bloqueados.](guidelines-for-securing-packages-on-locked-down-computers.md)
-   A partir de Windows Installer 3.0, la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) permite a los usuarios que no son administradores aplicar revisiones a las aplicaciones instaladas en el contexto por equipo. La aplicación de revisiones de UAC se habilita proporcionando un certificado de firmante en la tabla [MsiPatchCertificate](msipatchcertificate-table.md) y firmando revisiones con el mismo certificado.
-   La funcionalidad de Windows Installer 5.0 para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del Registro puede ayudar a proteger las aplicaciones de instalación. Para obtener información, vea [Securing Resources](securing-resources-.md).

 

 



