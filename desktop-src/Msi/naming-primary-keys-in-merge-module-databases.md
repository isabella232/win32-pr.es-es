---
description: Los nombres de las claves principales que una base de datos de módulo de mezcla debe cumplir una Convención de nomenclatura estándar.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Asignar nombres a las claves principales de las bases de datos de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544262"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Asignar nombres a las claves principales de las bases de datos de módulo de combinación

Los nombres de las claves principales que una base de datos de módulo de mezcla debe cumplir una Convención de nomenclatura estándar. La finalidad de esta Convención de nomenclatura es reducir la posibilidad de crear un conflicto de nombres entre las columnas de la tabla en el módulo de combinación y el paquete de instalación de destino. La Convención de nomenclatura no se puede aplicar a las tablas en las que la clave principal es un dato instalable. No aplique la Convención de nomenclatura a las tablas siguientes:

-   [Tabla MIME](mime-table.md)
-   [Tabla de extensión](extension-table.md)
-   [Tabla de iconos](icon-table.md)
-   [Tabla de verbos](verb-table.md)
-   [Tabla ProgId](progid-table.md)

Por ejemplo, no use para la clave principal de la tabla MIME porque es el tipo MIME y la aplicación del procedimiento de nomenclatura cambiaría su significado. En estos casos, los conflictos de nombres dependen del significado de los datos que sean únicos en todos los módulos.

El nombre de una clave principal de un módulo de combinación debe constar de un nombre legible anexado a una cadena realizada desde el GUID del módulo de combinación. Cada módulo de combinación debe tener su propio [*GUID*](g-gly.md). El GUID del módulo de combinación también debe crearse en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) del módulo de combinación. Los desarrolladores pueden crear GUID mediante una utilidad como GUIDGEN.

En el procedimiento siguiente se describe cómo generar una clave de base de datos principal que se adhiera a la Convención de nomenclatura estándar. Aplique el procedimiento siguiente solo a las tablas en las que la clave principal no sea datos que se van a instalar.

**Para asignar un nombre a una clave principal de un registro de tabla en un módulo de combinación**

1.  Cree la parte legible del nombre de la clave principal. Elija un nombre legible que identifique este registro, por ejemplo, MyRowEntry.
2.  Generar u obtener el GUID del módulo de combinación. Tenga en cuenta que todos los GUID deben crearse en mayúsculas. Para obtener más información acerca de los GUID, consulte [GUID](guid.md). El siguiente es un ejemplo de un GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. En los pasos siguientes, se modifica este valor en una cadena de caracteres que se debe anexar a cada nombre de clave principal del módulo de combinación.
3.  Quite las llaves del principio y el final del GUID.
4.  Cambie todos los guiones a carácter de subrayado.
5.  Anexe el resultado al final de la parte legible del nombre de la clave principal. Separe el nombre legible del GUID modificado por un punto. El nombre de la clave principal para el GUID de ejemplo indicado anteriormente se convierte en MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Repita el procedimiento para asignar un nombre a todas las claves principales de todas las tablas del módulo de combinación.

 

 



