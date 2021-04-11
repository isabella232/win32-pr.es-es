---
description: Las tablas del grupo procedimiento de instalación controlan las tareas realizadas durante la instalación por acciones estándar y acciones personalizadas.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Grupo de tablas de procedimientos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361550"
---
# <a name="installation-procedure-tables-group"></a>Grupo de tablas de procedimientos de instalación

Las tablas del grupo procedimiento de instalación controlan las tareas realizadas durante la instalación por [acciones estándar](standard-actions.md) y [acciones personalizadas](custom-actions.md).

Algunas de las tablas de este grupo controlan una acción de alto nivel proporcionando una secuencia de acciones. Cada una de las tablas de secuencia siguientes controla una parte de una acción de alto nivel.

-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabla AdminUISequence](adminuisequence-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla AdvtUISequence](advtuisequence-table.md)
-   [Tabla AdvtExecuteSequence](advtexecutesequence-table.md)

Puede haber situaciones en las que una instalación tenga que hacer algo que no sea posible mediante el uso de [acciones estándar](standard-actions.md)únicamente. Para proporcionar el mayor grado de flexibilidad, el instalador proporciona a los autores de la instalación la capacidad de crear sus propias acciones personalizadas. Si tiene alguna acción personalizada, debe registrarla con el instalador rellenando la tabla CustomAction.

La [tabla CustomAction](customaction-table.md) proporciona los medios para integrar el código personalizado y los datos en el proceso de instalación. El código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un ejecutable existente.

En las tablas siguientes se amplían las capacidades del instalador para manipular archivos y carpetas durante la instalación.

-   La [tabla RemoveFile](removefile-table.md) contiene una lista de archivos que se quitan durante la instalación.
-   La [tabla RemoveIniFile](removeinifile-table.md) contiene la información que necesita una aplicación para quitarse de los archivos. ini.
-   La [tabla RemoveRegistry](removeregistry-table.md) contiene la información que se elimina del registro del sistema cuando se selecciona el componente correspondiente para instalarse.
-   En la [tabla CreateFolder](createfolder-table.md) se enumeran las carpetas que se deben crear durante la instalación. Aunque el instalador crea carpetas a medida que se necesitan, se quitan tan pronto como están vacías. La lista de carpetas de la tabla CreateFolder no se elimina hasta que se desinstale el componente.
-   La [tabla MoveFile](movefile-table.md) contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado en el equipo del usuario a un directorio de destino. No es necesario usar la tabla MoveFile para describir los archivos asociados a los componentes que se van a instalar.

Para configurar las condiciones necesarias que se deben cumplir para iniciar la instalación, rellene la tabla LaunchCondition.

La [tabla LaunchCondition](launchcondition-table.md) contiene una lista de condiciones que se deben satisfacer para que la acción se realice correctamente.

 

 



