---
description: Windows Installer puede reparar, reemplazar y comprobar los archivos contenidos en una aplicación. Es posible que sea necesaria una reinstalación parcial o completa de la aplicación si faltan archivos o entradas del registro asociadas a alguna característica o están dañados.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Reinstalación de una característica o aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156460"
---
# <a name="reinstalling-a-feature-or-application"></a>Reinstalación de una característica o aplicación

Windows Installer puede reparar, reemplazar y comprobar los archivos contenidos en una aplicación. Es posible que sea necesaria una reinstalación parcial o completa de la aplicación si faltan archivos o entradas del registro asociadas a alguna característica o están dañados.

Cuando se vuelve a instalar una característica o aplicación, se reinstalan también todos los servicios, las variables de entorno y las acciones personalizadas que pertenecen a la característica o aplicación. Tenga en cuenta que esto significa que se perderán los cambios realizados en las variables de entorno entre la instalación original y la reinstalación.

La lista siguiente contiene métodos para reinstalar una característica o un producto. El instalador ha automatizado los dos primeros métodos:

-   Reparar, reemplazar o comprobar archivos mediante una llamada a la función [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) .
-   Vuelva a instalar todo el producto mediante una llamada a la función [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) .
-   Reinstale, reemplace o Compruebe los archivos con un botón de control de IU del instalador a través de la [reinstalación de ControlEvent,](reinstall-controlevent.md).
-   Reinstale, reemplace o Compruebe los archivos desde una línea de comandos. para ello, establezca la propiedad [**REINSTALL**](reinstall.md) y la propiedad [**REINSTALLMODE**](reinstallmode.md) .

Para obtener más información sobre la reinstalación de una característica o aplicación, consulte [resistencia](resiliency.md).

**Para reinstalar un producto mediante el instalador**

-   Llame a [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Para reinstalar una característica mediante el instalador**

-   Llame a [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

**Para reinstalar un producto o característica con una interfaz de usuario del instalador**

1.  Agregar un botón al cuadro de diálogo especificado mediante la adición de una entrada a la [tabla de control](control-table.md).
2.  Agregue un [ReinstallMode ControlEvent,](reinstallmode-controlevent.md) a la tabla ControlEvent,, con los campos de cuadro de diálogo \_ y control que \_ hacen referencia al control de botón creado en el paso 1. En el campo argumento, escriba una cadena que contenga las letras correspondientes a los modos de reinstalación que desee (los valores aceptables para este campo son idénticos a los aceptados para la propiedad [**REINSTALLMODE**](reinstallmode.md) ). El valor de la columna de ordenación de este evento debe ser 1.
3.  Agregue un evento [REINSTALL ControlEvent,](reinstall-controlevent.md) a la [tabla ControlEvent,](controlevent-table.md), de nuevo haciendo referencia al mismo control de botón. El campo de argumento de este evento será normalmente todos, para forzar la reinstalación de todas las características, pero puede colocar el nombre de una característica específica aquí. El valor de la columna de ordenación de este evento debe ser 2.
4.  Agregue un evento más asociado al mismo control de botón para iniciar realmente la reinstalación. Puede ser un evento EndDialog (con un argumento de Return). No obstante, lo más habitual es que se use aquí un evento NewDialog para saltar a un. **¿está seguro de que desea reinstalar?** cuadro de diálogo de confirmación. El valor de la columna de ordenación de este evento debe ser 3.

    Si lo desea, se pueden crear varios botones de [**reinstalación**](reinstall.md) para un único cuadro de diálogo, lo que permite al usuario seleccionar el tipo de reinstalación realizado. En este caso, cada botón se crea como se describe en el procedimiento anterior, con un parámetro [ReinstallMode ControlEvent,](reinstallmode-controlevent.md) diferente para cada botón.

Una vez que se ha instalado un determinado producto (con algunas o todas las características del producto), se puede realizar una reinstalación en la línea de comandos:

**Para reinstalar un producto o característica desde una línea de comandos**

1.  En el símbolo del sistema, especifique la propiedad [**REINSTALL**](reinstall.md) .
2.  En el símbolo del sistema, especifique la propiedad [**REINSTALLMODE**](reinstallmode.md) .

    Si se especifican estas propiedades, el usuario podrá volver a instalar todas las características del producto o todas ellas. También se puede especificar el tipo de reinstalación. Por ejemplo, puede especificar que solo se deben volver a instalar los archivos que faltan por completo, o que solo los archivos dañados (por ejemplo, cualquier archivo ejecutable cuya suma de comprobación no coincida con el contenido real del archivo) se reemplacen.

 

 



