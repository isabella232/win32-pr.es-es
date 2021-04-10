---
description: La creación de las tablas de secuencia es una parte esencial del desarrollo de un paquete del instalador porque estas tablas especifican el orden de ejecución de las acciones estándar que controlan el proceso de instalación y muestran los cuadros de diálogo de la interfaz de usuario.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Usar una tabla de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be10082aba05429a63df69444ed28bea350aa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910090"
---
# <a name="using-a-sequence-table"></a>Usar una tabla de secuencia

La creación de las tablas de secuencia es una parte esencial del desarrollo de un paquete del instalador porque estas tablas especifican el orden de ejecución de las [acciones estándar](standard-actions.md) que controlan el proceso de instalación y muestran los cuadros de diálogo de la interfaz de usuario.

Existen tres modos de instalación y dos tipos de tablas de secuencia para cada modo.

Los tres modos de instalación independientes que admite actualmente el instalador son los siguientes:

-   Instalación simple
-   Instalación administrativa
-   Instalación de anuncios

Cada una de las tablas de secuencia tiene tres campos: acción, condición y secuencia. El campo acción indica una acción estándar o personalizada, o un cuadro de diálogo o una secuencia definidos por el usuario que ejecuta el instalador. El campo condición permite al autor especificar una expresión lógica que controla si se ejecuta o se muestra un cuadro de diálogo de acción o definido por el usuario. Si el campo condición está en blanco o contiene una expresión que se evalúa como true, la acción o el cuadro de diálogo se ejecuta o se muestra. La acción o el cuadro de diálogo se omite si la expresión se evalúa como false. El campo Sequence especifica el orden de ejecución de cada acción o cuadro de diálogo definido por el usuario en la tabla.

Cada uno de estos modos de instalación procesa las tablas de secuencia de la interfaz de usuario y las tablas de secuencia de ejecución. Las tablas de secuencia de la interfaz de usuario solo se procesan si el instalador se inicializó con el nivel de presentación de la interfaz de usuario establecido en reducido o completo. Vea la referencia de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obtener más información acerca de los niveles de presentación de la interfaz de usuario.

Normalmente, las tablas de secuencia de la interfaz de usuario contienen acciones estándar relacionadas con la recopilación de información del sistema que se muestra al usuario a través de la interfaz de usuario. La interfaz de usuario se muestra grabando las claves externas en los nombres de los cuadros de diálogo de la [tabla de diálogo](dialog-table.md) en el campo acción de la tabla de secuencia de la interfaz de usuario. A continuación, el usuario tiene la oportunidad de modificar o aceptar la información del sistema e iniciar la instalación, que se produce cuando se procesa la tabla de secuencia de ejecución.

Durante una instalación simple, se ejecuta la acción instalar de nivel superior que, [a](install-action.md) su vez, procesa la [tabla InstallUISequence](installuisequence-table.md) y la [tabla InstallExecuteSequence](installexecutesequence-table.md).

Una instalación administrativa suele ser iniciada por un administrador de red para asignar e instalar aplicaciones para usuarios individuales y grupos de usuarios. Durante este tipo de instalación, se ejecuta la acción de nivel superior [admin](admin-action.md) que procesa la [tabla AdminUISequence](adminuisequence-table.md) y la [tabla AdminExecuteSequence](adminexecutesequence-table.md).

Para [anunciar](advertisement.md) una aplicación o característica, el instalador se debe iniciar con la acción [anunciar](advertise-action.md) . Durante este tipo de instalación, se procesa la [tabla AdvtExecuteSequence](advtexecutesequence-table.md) .

Al crear una tabla de secuencia, se recomienda usar el número de secuencia para las acciones estándar de las secuencias sugeridas en los temas siguientes. En el caso de las acciones estándar que no tienen ninguna posición estándar en la tabla de secuencia, como [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)y [InstallExecute](installexecute-action.md), use un número de secuencia que sea un múltiplo de diez para identificar la acción como una acción estándar. En el caso de las acciones personalizadas, utilice un número de secuencia que no sea múltiplo de diez para diferenciarlo de las acciones estándar en la tabla de secuencia.

Para ver las secuencias de acción sugeridas para cada tabla de secuencia, vea los temas siguientes:

-   [InstallUISequence sugerido](suggested-installuisequence.md)
-   [InstallExecuteSequence sugerido](suggested-installexecutesequence.md)
-   [AdminUISequence sugerido](suggested-adminuisequence.md)
-   [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)
-   [AdvtUISequence sugerido](suggested-advtuisequence.md)
-   [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)

Para obtener una descripción detallada de las tablas de secuencia y cómo se ejecutan las acciones estándar, vea el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

* * Windows Installer 3,0 y versiones posteriores: * *

A partir de Windows Installer 3,0, un paquete de revisión puede contener la [tabla MsiPatchSequence](msipatchsequence-table.md). Esta tabla contiene toda la información que el instalador necesita para determinar la secuencia de la aplicación de una revisión de actualización pequeña en relación con todas las demás revisiones. Para obtener más información, consulte [revisiones y actualizaciones](patching-and-upgrades.md).

> [!Note]
>
> Los [módulos de combinación](merge-modules.md) pueden contener tablas de base de datos de módulos de [mezcla](merge-module-database-tables.md) que modifican las tablas de secuencia de acciones del archivo. msi de destino. La combinación del módulo en una base de datos puede modificar la información de la tabla de secuencia, pero no agrega estas tablas al archivo. msi. Para obtener más información, vea [creación de tablas de secuencia de módulo de combinación](authoring-merge-module-sequence-tables.md).

 

 

 



