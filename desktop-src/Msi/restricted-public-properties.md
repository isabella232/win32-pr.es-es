---
description: En algunos casos, un usuario que no es administrador del sistema solo puede reemplazar una lista aprobada de propiedades públicas de Windows Installer restringidas.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propiedades públicas restringidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652919"
---
# <a name="restricted-public-properties"></a>Propiedades públicas restringidas

En el caso de una instalación administrada, es posible que el autor del paquete tenga que limitar las [propiedades públicas](public-properties.md) que se pasan al lado servidor y que un usuario que no es administrador del sistema puede cambiar. Normalmente, algunas restricciones son necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados. Si se cumplen todas las condiciones siguientes, un usuario que no sea administrador del sistema solo puede reemplazar una lista aprobada de propiedades públicas restringidas:

-   El sistema es Windows 2000.
-   El usuario no es un administrador del sistema.
-   La aplicación o el producto se está instalando con privilegios elevados.

Si se cumplen todas las condiciones anteriores, el instalador tiene como valor predeterminado la siguiente lista de propiedades públicas restringidas que cualquier usuario puede cambiar:

-   [**ACTUAR**](action.md)
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
-   [**NoCompanyName**](nocompanyname.md)
-   [**NoUserName**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**DISTRIBUCIÓN**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**REINICIO**](reboot.md)
-   [**REINSTALAR**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**RECUPER**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**TRANSFORMA**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

El autor de un paquete de instalación puede extender esta lista predeterminada para incluir propiedades públicas adicionales mediante la propiedad [**SecureCustomProperties**](securecustomproperties.md) .

Al establecer la propiedad [**EnableUserControl**](-enableusercontrol.md) o la [Directiva del sistema](system-policy.md) [EnableUserControl](enableusercontrol.md), la lista se amplía a todas las propiedades públicas. A continuación, todos los usuarios pueden cambiar cualquier propiedad pública.

El instalador establece la propiedad [**RestrictedUserControl**](restrictedusercontrol.md) cada vez que se restringe la lista de propiedades públicas que los usuarios que no son administradores pasan al servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> </dl>

 

 



