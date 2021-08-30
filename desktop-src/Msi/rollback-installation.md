---
description: Cuando el instalador de Windows procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Instalación de reversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276cec7d16cf5344a778dfb894d7e03e81190be42cb10f4438f128a2c3d1fed6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039895"
---
# <a name="rollback-installation"></a>Instalación de reversión

Cuando el instalador de Windows procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación. Estos archivos se mantienen en un directorio del sistema oculto y se eliminan automáticamente una vez completada correctamente la instalación. Sin embargo, si la instalación no se realiza correctamente, el instalador realiza automáticamente una instalación de reversión que devuelve el sistema a su estado original.

La reversión automática de una instalación incorrecta es el comportamiento predeterminado del instalador. Para deshabilitar la reversión durante una instalación, use una de las siguientes opciones:

-   [**DisableROLLBACK, propiedad**](-disablerollback.md)
-   [**Propiedad PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Acción DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent](enablerollback-controlevent.md)

Cada vez que se deshabilita la reversión, el instalador establece [**la propiedad RollbackDisabled.**](rollbackdisabled.md)

Si una instalación usa [acciones personalizadas,](custom-actions.md)se requiere la creación adicional del paquete de instalación para usar la funcionalidad de reversión. Para obtener más información, [vea Reversión de acciones personalizadas.](rollback-custom-actions.md)

 

 



