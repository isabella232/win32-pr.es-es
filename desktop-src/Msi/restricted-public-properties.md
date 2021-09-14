---
description: En determinados casos, un usuario que no es un administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas Windows installer.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propiedades públicas restringidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246386"
---
# <a name="restricted-public-properties"></a>Propiedades públicas restringidas

En el caso de una instalación administrada, es [](public-properties.md) posible que el autor del paquete deba limitar qué propiedades públicas se pasan al lado del servidor y que un usuario que no sea administrador del sistema pueda cambiar. Algunas restricciones son normalmente necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados. Si se cumplen todas las condiciones siguientes, un usuario que no sea administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas restringidas:

-   El sistema es Windows 2000.
-   El usuario no es un administrador del sistema.
-   La aplicación o el producto se instala con privilegios elevados.

Si se cumplen todas las condiciones anteriores, el instalador tiene como valor predeterminado la siguiente lista de propiedades públicas restringidas que cualquier usuario puede cambiar:

-   [**ACCIÓN**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NOCOMPANYNAME**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**PATCH**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**REINICIAR**](reboot.md)
-   [**REINSTALAR**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**REANUDAR**](resume.md)
-   [**SECUENCIA**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**TRANSFORMA**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

El autor de un paquete de instalación puede ampliar esta lista predeterminada para incluir propiedades públicas adicionales mediante la [**propiedad SecureCustomProperties.**](securecustomproperties.md)

Al establecer [**la propiedad EnableUserControl**](-enableusercontrol.md) o la directiva del sistema [EnableUserControl,](enableusercontrol.md)[](system-policy.md) se amplía la lista a todas las propiedades públicas. A continuación, todos los usuarios pueden cambiar cualquier propiedad pública.

El instalador establece la [**propiedad RestrictedUserControl**](restrictedusercontrol.md) cada vez que se restringe la lista de propiedades públicas que los usuarios que no son administradores pasan al servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> </dl>

 

 



