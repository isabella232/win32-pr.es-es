---
description: Cuando el Windows Installer procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Revertir instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155512"
---
# <a name="rollback-installation"></a>Revertir instalación

Cuando el Windows Installer procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación. Estos archivos se conservan en un directorio oculto del sistema y se eliminan automáticamente una vez completada correctamente la instalación. Si no es así, el instalador realiza automáticamente una instalación de reversión que devuelve el sistema a su estado original.

La reversión automática de una instalación incorrecta es el comportamiento predeterminado del instalador. Para deshabilitar la reversión durante una instalación, use uno de los siguientes:

-   [**Propiedad DISABLEROLLBACK**](-disablerollback.md)
-   [**Propiedad PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Acción DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent,](enablerollback-controlevent.md)

Cada vez que se deshabilita la reversión, el instalador establece la propiedad [**RollbackDisabled**](rollbackdisabled.md) .

Si una instalación utiliza [acciones personalizadas](custom-actions.md), se requiere la creación de un paquete de instalación adicional para usar la funcionalidad de reversión. Para obtener más información, consulte [reversión de acciones personalizadas](rollback-custom-actions.md).

 

 



