---
description: La creación de las tablas de secuencia es una parte esencial del desarrollo de un paquete del instalador porque estas tablas especifican el orden de ejecución de las acciones estándar que controlan el proceso de instalación y muestran los cuadros de diálogo de la interfaz de usuario.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Usar una tabla de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809015"
---
# <a name="using-a-sequence-table"></a>Usar una tabla de secuencias

La creación de las tablas de secuencia es una parte esencial del desarrollo de [](standard-actions.md) un paquete del instalador porque estas tablas especifican el orden de ejecución de las acciones estándar que controlan el proceso de instalación y muestran los cuadros de diálogo de la interfaz de usuario.

Hay tres modos de instalación y dos tipos de tablas de secuencia para cada modo.

Los tres modos de instalación independientes admitidos actualmente por el instalador son:

-   Instalación simple
-   Instalación administrativa
-   Instalación de anuncios

Cada una de las tablas de secuencia tiene tres campos: Acción, Condición y Secuencia. El campo Acción nombra una acción estándar o personalizada o un cuadro de diálogo definido por el usuario o secuencia que ejecuta el instalador. El campo Condición permite al autor especificar una expresión lógica que controla si se ejecuta o muestra una acción o un diálogo definido por el usuario. Si el campo Condición está en blanco o contiene una expresión que se evalúa como True, se ejecuta o se muestra la acción o el cuadro de diálogo. La acción o el cuadro de diálogo se omite si la expresión se evalúa como False. El campo Secuencia especifica el orden de ejecución de cada acción o cuadro de diálogo definido por el usuario de la tabla.

Cada uno de estos modos de instalación procesa las tablas de secuencia de la interfaz de usuario y las tablas de secuencia de ejecución. Las tablas de secuencia de la interfaz de usuario solo se procesan si el instalador se inicializó con el nivel de presentación de la interfaz de usuario establecido en Reducido o Completo. Consulte la [**referencia de MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obtener más información sobre los niveles de presentación de la interfaz de usuario.

Las tablas de secuencias de la interfaz de usuario normalmente contienen acciones estándar relacionadas con la recopilación de información del sistema que se muestran al usuario a través de la interfaz de usuario. La interfaz de usuario se muestra registrando las claves [](dialog-table.md) externas en los nombres de los cuadros de diálogo de la tabla de diálogos en el campo Acción de la tabla de secuencias de la interfaz de usuario. A continuación, el usuario tiene la oportunidad de modificar o aceptar la información del sistema y comenzar la instalación, lo que se produce cuando se procesa la tabla de secuencia de ejecución.

Durante una instalación sencilla, se ejecuta la acción de nivel superior [INSTALL](install-action.md) que, a su vez, procesa la tabla [InstallUISequence](installuisequence-table.md) y la [tabla InstallExecuteSequence](installexecutesequence-table.md).

Normalmente, un administrador de red inicia una instalación administrativa para asignar e instalar aplicaciones para usuarios individuales y grupos de usuarios. Durante este tipo de instalación, se ejecuta la acción de nivel superior [ADMIN](admin-action.md) que procesa la [tabla AdminUISequence](adminuisequence-table.md) y la [tabla AdminExecuteSequence](adminexecutesequence-table.md).

Para [anunciar](advertisement.md) una aplicación o característica, el instalador debe iniciarse con la [acción ADVERTISE.](advertise-action.md) Durante este tipo de instalación se procesa la tabla [AdvtExecuteSequence.](advtexecutesequence-table.md)

Al crear cualquier tabla de secuencias, se recomienda usar el número de secuencia para las acciones estándar de las secuencias sugeridas en los temas siguientes. Para las acciones estándar que no tienen ninguna posición estándar en la tabla de secuencias, como [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)e [InstallExecute,](installexecute-action.md)use un número de secuencia que sea un múltiplo de diez para identificar la acción como una acción estándar. Para las acciones personalizadas, use un número de secuencia que no sea un múltiplo de diez para diferenciarlo de las acciones estándar de la tabla de secuencia.

Para obtener secuencias de acciones sugeridas para cada tabla de secuencias, vea los temas siguientes:

-   [InstallUISequence sugerido](suggested-installuisequence.md)
-   [Instalación sugeridaExecuteSequence](suggested-installexecutesequence.md)
-   [AdminUISequence sugerido](suggested-adminuisequence.md)
-   [Administración sugeridaExecuteSequence](suggested-adminexecutesequence.md)
-   [AdvtUISequence sugerido](suggested-advtuisequence.md)
-   [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)

Para obtener una descripción detallada de las tablas de secuencia y cómo se ejecutan las acciones estándar, vea el ejemplo detallado de la tabla [de secuencia .](sequence-table-detailed-example.md)

**Windows Installer 3.0 y versiones posteriores: **

A partir Windows Installer 3.0, un paquete de revisión puede contener la [tabla MsiPatchSequence](msipatchsequence-table.md). Esta tabla contiene toda la información que requiere el instalador para determinar la secuencia de la aplicación de una revisión de actualización pequeña en relación con todas las demás revisiones. Para obtener más información, vea [Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)

> [!Note]
>
> [Los módulos de](merge-modules.md) mezcla pueden contener [tablas de base de datos de módulos de mezcla](merge-module-database-tables.md) que modifican las tablas de secuencia de acciones del archivo .msi destino. La combinación del módulo en una base de datos puede modificar la información de la tabla de secuencia, pero no agrega estas tablas al archivo .msi secuencia. Para obtener más información, vea [Crear tablas de secuencias de módulos de mezcla](authoring-merge-module-sequence-tables.md).

 

 

 



