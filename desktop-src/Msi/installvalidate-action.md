---
description: La acción InstallValidate comprueba que todos los volúmenes a los que se ha atribuido el costo tienen espacio suficiente para la instalación. La acción InstallValidate finaliza la instalación con un error irreales si algún volumen no tiene espacio en disco.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Acción InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8a5e2f69df5e588c2366f7cf9fff0fb3621889e9b725605a38acc14f39457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805643"
---
# <a name="installvalidate-action"></a>Acción InstallValidate

La acción InstallValidate comprueba [](v-gly.md) que [](c-gly.md) todos los volúmenes a los que se ha atribuido el costo tienen espacio suficiente para la instalación. La acción InstallValidate finaliza la instalación con un error irreales si algún volumen no tiene espacio en disco.

La acción InstallValidate también notifica al usuario si un proceso activo está utilizando actualmente uno o varios archivos que se van a sobrescribir o quitar. Para obtener más información, vea [Reinicios del sistema.](system-reboots.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción CostFinalize](costfinalize-action.md) y las secuencias de cuadro de diálogo de la interfaz de usuario que permiten al usuario modificar los estados de selección o directorios deben secuenciarse antes de la acción InstallValidate.

[Las acciones personalizadas](custom-actions.md) que cambian el estado de instalación de características o componentes deben secuenciarse antes de la acción InstallValidate.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

Normalmente, una secuencia de cuadro de diálogo de interfaz de usuario anterior debe realizar la misma comprobación que la acción InstallValidate cuando el usuario intenta iniciar la copia de archivos. Esta secuencia de cuadro  de diálogo de interfaz de usuario debe presentar un cuadro de diálogo Espacio insuficiente en disco si los volúmenes seleccionados no tienen suficiente espacio para la instalación. Los cuadros de diálogo de la interfaz de usuario deben crearse de forma que el usuario no pueda continuar con la instalación si no hay suficiente espacio en disco. En el caso de una instalación silenciosa, no hay ninguna interfaz de usuario y la acción InstallValidate finaliza la instalación si no hay suficiente espacio en disco. La causa de la terminación prematura se registra en el archivo de registro si el registro está habilitado.

Una entrada se agrega a una tabla Interna FilesInUse si algún archivo se sobrescribe o se quita mientras está abierto para su ejecución o modificación por cualquier proceso durante el costo del [*archivo.*](c-gly.md) La tabla FilesInUse contiene columnas para el nombre y la ruta de acceso completa del archivo. Cuando se ejecuta la acción InstallValidate, el instalador consulta la tabla FilesInUse en busca de entradas y determina el nombre del proceso mediante el archivo . La acción InstallValidate agrega un registro a la tabla de interfaz de usuario [listBox](listbox-table.md) para cada proceso único identificado por esta consulta. El registro contiene los siguientes valores en cada columna:

**Propiedad**: FileInUseProcess

 

**Valor:** *nombre del proceso*

 

**Texto:** *texto contenido en el título de la ventana principal del proceso*

A continuación, la acción InstallValidate muestra **el cuadro de diálogo Archivos** en uso . En este cuadro de diálogo se muestran los procesos que se deben apagar para evitar la necesidad de reiniciar el sistema para reemplazar los archivos en uso.

La acción InstallValidate consulta en la tabla [Dialog](dialog-table.md) un cuadro de diálogo creado con el nombre reservado [FilesInUse](filesinuse-dialog.md) dialog y lo muestra. Este cuadro de diálogo debe contener un control [ListBox](listbox-control.md) que esté vinculado a una propiedad denominada FileInUseProcess. Por convención, este cuadro de diálogo  tiene **un botón Salir,** **Reintentar** o Omitir, pero es el autor de la interfaz de usuario. Cada botón debe estar asociado a [un control EndDialog](enddialog-controlevent.md) En la [tabla ControlEvent.](controlevent-table.md) La acción InstallValidate responde como se indica a continuación al valor devuelto por [doAction](doaction-controlevent.md) ControlEvent, tal como lo dicta uno de estos argumentos [endDialog](enddialog-controlevent.md) asociados con el botón presionado por el usuario:

**Reintentar:** se borran todos los valores agregados [](c-gly.md) a la tabla [ListBox](listbox-table.md) y se repite todo el procedimiento de costo de archivos, y se vuelve a comprobar los archivos que todavía están en uso. Si uno o varios procesos todavía se identifican como archivos que se van a sobrescribir o eliminar, el proceso se repite. De lo contrario, InstallValidate devuelve el control al instalador con el estado msiDoActionStatusSuccess.

**Exit:** la acción InstallValidate devuelve inmediatamente el control al instalador con el estado msiDoActionStatusUserExit. Esto finaliza la instalación.

**Cualquier otro valor devuelto:** la acción InstallValidate devuelve inmediatamente el control al instalador con el estado msiDoActionStatusSuccess. En este caso, dado que uno o varios archivos siguen en uso, las acciones [InstallFiles](installfiles-action.md) o [InstallAdminPackage](installadminpackage-action.md) posteriores deben programar los archivos en uso que se reemplazarán o eliminarán cuando se reinicie el sistema.

Si no hay ninguna [tabla ListBox](listbox-table.md) en la base de datos, InstallValidate se cierra en modo silencioso sin errores.

El punto y coma es el delimitador de lista para transformaciones, orígenes y revisiones, y no debe usarse en estos nombres de archivo o rutas de acceso.

El instalador nunca considera en uso los archivos marcados como de solo lectura en una ubicación de solo lectura.

Si el **nivel de interfaz de**  usuario es básico, se presenta al usuario un cuadro de diálogo Predeterminado de espacio en disco que contiene los botones Anular y Reintentar. 

 

 



