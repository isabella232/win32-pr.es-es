---
description: Los nombres de las claves principales de una base de datos de módulos de combinación deben cumplir una convención de nomenclatura estándar.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Nomenclatura de claves principales en bases de datos de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261060"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Nomenclatura de claves principales en bases de datos de módulos de mezcla

Los nombres de las claves principales de una base de datos de módulos de combinación deben cumplir una convención de nomenclatura estándar. El propósito de esta convención de nomenclatura es reducir la posibilidad de crear un conflicto de nombres entre las columnas de tabla del módulo de mezcla y el paquete de instalación de destino. La convención de nomenclatura no se puede aplicar a las tablas en las que la clave principal es datos instalables. No aplique la convención de nomenclatura a las tablas siguientes:

-   [Tabla MIME](mime-table.md)
-   [Tabla de extensiones](extension-table.md)
-   [Tabla de iconos](icon-table.md)
-   [Tabla de verbos](verb-table.md)
-   [Tabla ProgId](progid-table.md)

Por ejemplo, no use para la clave principal de la tabla MIME porque este es el tipo MIME y aplicar el procedimiento de nomenclatura cambiaría su significado. En estos casos, los conflictos de nombres dependen del significado de que los datos sean únicos entre módulos.

El nombre de una clave principal en un módulo de combinación debe constar de un nombre legible anexado con una cadena realizada a partir del GUID del módulo de mezcla. Cada módulo de combinación debe tener su propio [*GUID.*](g-gly.md) El GUID del módulo de mezcla también debe crearse en la propiedad [**Resumen**](revision-number-summary.md) del número de revisión del módulo de mezcla. Los desarrolladores pueden crear GUID mediante una utilidad como GUIDGEN.

En el procedimiento siguiente se describe cómo generar una clave de base de datos principal que cumpla la convención de nomenclatura estándar. Aplique el procedimiento siguiente solo a las tablas en las que la clave principal no son datos que se están instalando.

**Para dar nombre a una clave principal de un registro de tabla en un módulo de combinación**

1.  Cree la parte legible del nombre de la clave principal. Elija un nombre legible que identifique este registro, por ejemplo, MyRowEntry.
2.  Genere u obtenga el GUID del módulo de combinación. Tenga en cuenta que todos los GUID deben crearse en mayúsculas. Para obtener más información acerca de los GUID, vea [GUID](guid.md). El siguiente es un ejemplo de un GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. En los pasos siguientes se modifica en una cadena de caracteres que se debe anexar a cada nombre de clave principal del módulo merge.
3.  Quite las llaves del principio y el final del GUID.
4.  Cambie todos los guiones a caracteres de subrayado.
5.  Anexe el resultado al final de la parte legible del nombre de clave principal. Separe el nombre legible del GUID modificado por un punto. El nombre de clave principal del GUID de ejemplo anterior se convierte en MyRowEntry.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Repita esta operación para dar nombre a todas las claves principales de todas las tablas del módulo merge.

 

 



