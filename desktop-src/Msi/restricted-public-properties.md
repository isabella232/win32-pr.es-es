---
description: En determinados casos, un usuario que no sea un administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas Windows instalador restringido.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propiedades públicas restringidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af09200f10261e50564ae79dbad961474d23d8a6354cee7344aa107c8b73fb57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979305"
---
# <a name="restricted-public-properties"></a>Propiedades públicas restringidas

En el caso de una instalación administrada, es [](public-properties.md) posible que el autor del paquete tenga que limitar las propiedades públicas que se pasan al lado servidor y que puede cambiar un usuario que no sea administrador del sistema. Algunas restricciones son normalmente necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados. Si se cumplen todas las condiciones siguientes, un usuario que no sea administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas restringidas:

-   El sistema es Windows 2000.
-   El usuario no es un administrador del sistema.
-   La aplicación o el producto se instala con privilegios elevados.

Si se cumplen todas las condiciones anteriores, el instalador tiene como valor predeterminado la siguiente lista de propiedades públicas restringidas que cualquier usuario puede cambiar:

-   [**Acción**](action.md)
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
-   [**Parche**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**Reiniciar**](reboot.md)
-   [**Reinstalar**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**Reanudar**](resume.md)
-   [**Secuencia**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**Transforma**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

El autor de un paquete de instalación puede ampliar esta lista predeterminada para incluir propiedades públicas adicionales mediante la [**propiedad SecureCustomProperties.**](securecustomproperties.md)

Al establecer [**la propiedad EnableUserControl**](-enableusercontrol.md) o la directiva del sistema [EnableUserControl,](enableusercontrol.md)[se](system-policy.md) amplía la lista a todas las propiedades públicas. A continuación, todos los usuarios pueden cambiar cualquier propiedad pública.

El instalador establece la [**propiedad RestrictedUserControl**](restrictedusercontrol.md) cada vez que se restringe la lista de propiedades públicas que los usuarios que no son administradores pasan al servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> </dl>

 

 



