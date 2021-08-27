---
description: Windows El instalador puede reparar, reemplazar y comprobar los archivos contenidos en una aplicación. Es posible que se requiera una reinstalación parcial o completa de la aplicación si faltan archivos o entradas del Registro asociadas a alguna característica o están dañadas.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Reinstalación de una característica o aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803fc3271cb69280ae84ae096e7a411dbf599f0a321bf15baac6dbd5ca8e1512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086005"
---
# <a name="reinstalling-a-feature-or-application"></a>Reinstalación de una característica o aplicación

Windows El instalador puede reparar, reemplazar y comprobar los archivos contenidos en una aplicación. Es posible que se requiera una reinstalación parcial o completa de la aplicación si faltan archivos o entradas del Registro asociadas a alguna característica o están dañadas.

Cuando se reinstala una característica o aplicación, también se reinstalan todos los servicios, variables de entorno y acciones personalizadas que pertenecen a la característica o aplicación. Tenga en cuenta que esto significa que se pierden los cambios realizados en las variables de entorno entre la instalación original y la reinstalación.

La lista siguiente contiene métodos para reinstalar una característica o un producto. El instalador ha automatizado los dos primeros métodos:

-   Repare, reemplace o compruebe los archivos mediante una llamada a [**la función MsiReinstallFeature.**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   Vuelva a instalar todo el producto llamando a [**la función MsiReinstallProduct.**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   Vuelva a instalar, reemplazar o comprobar los archivos con un botón de control de interfaz de usuario del instalador a través [de Reinstall ControlEvent](reinstall-controlevent.md).
-   Reinstale, reemplace o compruebe los archivos desde una línea de comandos estableciendo la propiedad [**REINSTALL**](reinstall.md) y la [**propiedad REINSTALLMODE.**](reinstallmode.md)

Para obtener más información sobre cómo reinstalar una característica o aplicación, vea [Resistencia](resiliency.md).

**Para volver a instalar un producto mediante el instalador**

-   Llame [**a MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Para volver a instalar una característica mediante el instalador**

-   Llame [**a MsiReinstallFeature.**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)

**Para volver a instalar un producto o una característica con una interfaz de usuario del instalador**

1.  Agregue un botón al cuadro de diálogo especificado agregando una entrada a la [tabla Control](control-table.md).
2.  Agregue un [control ReinstallMode ControlEvent](reinstallmode-controlevent.md) a la tabla ControlEvent, con los campos Dialog y Control que hacen referencia al control de botón creado \_ en el paso \_ 1. En el campo Argumento, escriba una cadena que contenga las letras correspondientes a los modos de reinstalación que desee (los valores aceptables para este campo son idénticos a los aceptados para la [**propiedad REINSTALLMODE).**](reinstallmode.md) El valor de la columna Ordering de este evento debe ser 1.
3.  Agregue un [evento Reinstall ControlEvent](reinstall-controlevent.md) a la [tabla ControlEvent](controlevent-table.md)y vuelva a hacer referencia al mismo control de botón. El campo Argumento de este evento normalmente será ALL, para forzar la reinstalación de todas las características, pero aquí puede colocar el nombre de una característica específica. El valor de la columna Ordering de este evento debe ser 2.
4.  Agregue un evento más asociado al mismo control de botón para iniciar realmente la reinstalación. Puede ser un evento EndDialog (con un argumento return). Sin embargo, lo más habitual es que aquí se utilice un evento NewDialog para saltar a un cuadro de diálogo de confirmación ¿Está seguro de que desea **reinstalar?** . El valor de la columna Ordering de este evento debe ser 3.

    Si lo desea, se pueden crear varios botones [**REINSTALL**](reinstall.md) para un único cuadro de diálogo, lo que permite al usuario seleccionar el tipo de reinstalación realizada. En este caso, cada botón se ha escrito como se describe en el procedimiento anterior, con un parámetro [ReinstallMode ControlEvent](reinstallmode-controlevent.md) diferente para cada botón.

Una vez instalado un producto determinado (con algunas o todas las características del producto), se puede realizar una reinstalación en la línea de comandos:

**Para volver a instalar un producto o una característica desde una línea de comandos**

1.  En el símbolo del sistema, especifique la [**propiedad REINSTALL.**](reinstall.md)
2.  En el símbolo del sistema, especifique la [**propiedad REINSTALLMODE.**](reinstallmode.md)

    La especificación de estas propiedades permite al usuario volver a instalar cualquiera o todas las características del producto. También se puede especificar el tipo de reinstalación. Por ejemplo, puede especificar que solo se vuelvan a instalar los archivos que faltan completamente o que solo se reemplazen los archivos dañados (por ejemplo, cualquier archivo ejecutable cuya suma de comprobación no coincida con el contenido real del archivo).

 

 



