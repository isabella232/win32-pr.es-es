---
description: Las tablas del grupo Procedimiento de instalación controlan las tareas realizadas durante la instalación por acciones estándar y acciones personalizadas.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Grupo de tablas de procedimientos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c66cc377fdf36969699f0e150fc30a02363ed24aa1848c4492917bffda7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633590"
---
# <a name="installation-procedure-tables-group"></a>Grupo de tablas de procedimientos de instalación

Las tablas del grupo Procedimiento de instalación controlan las tareas realizadas durante la instalación por acciones [estándar](standard-actions.md) y [acciones personalizadas](custom-actions.md).

Algunas de las tablas de este grupo controlan una acción de alto nivel proporcionando una secuencia de acciones. Cada una de las siguientes tablas de secuencia controla una parte de una acción de alto nivel.

-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabla AdminUISequence](adminuisequence-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla AdvtUISequence](advtuisequence-table.md)
-   [Tabla AdvtExecuteSequence](advtexecutesequence-table.md)

Puede haber situaciones en las que una instalación tenga que hacer algo que no sea posible usando solo [acciones estándar.](standard-actions.md) Para proporcionar el mayor grado de flexibilidad, el instalador proporciona a los autores de la instalación la capacidad de crear sus propias acciones personalizadas. Si tiene alguna acción personalizada, debe registrarlas con el instalador mediante la rellenar la tabla CustomAction.

La [tabla CustomAction proporciona](customaction-table.md) los medios para integrar el código y los datos personalizados en el proceso de instalación. El código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.

Las tablas siguientes amplían las funcionalidades del instalador para manipular archivos y carpetas durante la instalación.

-   La [tabla RemoveFile contiene](removefile-table.md) una lista de archivos que se quitan durante la instalación.
-   La [tabla RemoveIniFile](removeinifile-table.md) contiene la información que una aplicación debe quitar de .ini archivos.
-   La [tabla RemoveRegistry](removeregistry-table.md) contiene la información que se elimina del registro del sistema cuando se selecciona instalar el componente correspondiente.
-   En [la tabla CreateFolder se](createfolder-table.md) enumeran las carpetas que se deben crear durante la instalación. Aunque el instalador crea carpetas a medida que son necesarias, se quitan en cuanto están vacías. La lista de carpetas de la tabla CreateFolder no se elimina hasta que se desinstala el componente.
-   La [tabla MoveFile](movefile-table.md) contiene una lista de archivos que se van a mover o copiar desde un directorio de origen especificado del equipo del usuario a un directorio de destino. No es necesario usar la tabla MoveFile para describir los archivos asociados a los componentes que va a instalar.

Para configurar las condiciones necesarias que se deben cumplir para iniciar la instalación, rellene la tabla LaunchCondition.

La [tabla LaunchCondition contiene](launchcondition-table.md) una lista de condiciones, todas las cuales deben cumplirse para que la acción se ejecute correctamente.

 

 



