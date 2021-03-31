---
description: La acción InstallValidate comprueba que todos los volúmenes a los que se ha atribuido el costo tienen suficiente espacio para la instalación. La acción InstallValidate finaliza la instalación con un error irrecuperable si algún volumen tiene poco espacio en disco.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Acción InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278608"
---
# <a name="installvalidate-action"></a>Acción InstallValidate

La acción InstallValidate comprueba que todos los [*volúmenes*](v-gly.md) a los que se ha atribuido el [*costo*](c-gly.md) tienen suficiente espacio para la instalación. La acción InstallValidate finaliza la instalación con un error irrecuperable si algún volumen tiene poco espacio en disco.

La acción InstallValidate también notifica al usuario si uno o varios archivos que se van a sobrescribir o quitar están actualmente en uso por un proceso activo. Para obtener más información, consulte [reinicios del sistema](system-reboots.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción [CostFinalize](costfinalize-action.md) y las secuencias del cuadro de diálogo de la interfaz de usuario que permiten al usuario modificar los Estados y/o directorios de selección se deben secuenciar antes de la acción InstallValidate.

Las [acciones personalizadas](custom-actions.md) que cambian el estado de la instalación de las características o componentes deben secuenciarse antes de la acción InstallValidate.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

Normalmente, una secuencia del cuadro de diálogo de la interfaz de usuario anterior debe realizar la misma comprobación que la acción InstallValidate cuando el usuario intenta iniciar la copia de archivos. Esta secuencia del cuadro de diálogo de la interfaz de usuario debe presentar un cuadro **de diálogo de espacio** insuficiente en el disco si los volúmenes seleccionados no tienen suficiente espacio para la instalación. Los cuadros de diálogo de la interfaz de usuario deben crearse de forma que el usuario no pueda continuar con la instalación si no hay suficiente espacio en disco. En el caso de una instalación silenciosa, no hay ninguna interfaz de usuario y la acción InstallValidate finaliza la instalación si no hay suficiente espacio en disco. La causa de la finalización prematura se registra en el archivo de registro si está habilitado el registro.

Se agrega una entrada a una tabla FilesInUse interna si se sobrescribe o se quita un archivo mientras está abierto para su ejecución o modificación por parte de cualquier proceso durante el [*costo*](c-gly.md)de los archivos. La tabla FilesInUse contiene columnas para el nombre y la ruta de acceso completa del archivo. Cuando se ejecuta la acción InstallValidate, el instalador consulta la tabla FilesInUse para buscar entradas y determina el nombre del proceso mediante el archivo. La acción InstallValidate agrega un registro a la tabla de la interfaz de usuario de [ListBox](listbox-table.md) para cada proceso único identificado por esta consulta. El registro contiene los siguientes valores en cada columna:

**Propiedad**: FileInUseProcess

 

**Valor**: *nombre del proceso*

 

**Texto**: *texto contenido en el título de la ventana principal del proceso*

A continuación, la acción InstallValidate muestra el cuadro **de diálogo archivos en uso** . Este cuadro de diálogo muestra los procesos que deben cerrarse para evitar el requisito de reiniciar el sistema para reemplazar los archivos en uso.

La acción InstallValidate consulta la tabla de [diálogo](dialog-table.md) de un cuadro de diálogo creado con el cuadro de diálogo nombre reservado [FilesInUse](filesinuse-dialog.md) y lo muestra. Este cuadro de diálogo debe contener un control [ListBox](listbox-control.md) que esté asociado a una propiedad denominada FileInUseProcess. Por Convención, este cuadro de diálogo tiene un botón **salir**, **Reintentar** u **omitir** , pero es el autor de la interfaz de usuario. Cada botón debe estar vinculado a un ControlEvent, [EndDialog](enddialog-controlevent.md) en la tabla [ControlEvent,](controlevent-table.md) . La acción InstallValidate responde como se indica a continuación al valor devuelto por el ControlEvent, de la [acción](doaction-controlevent.md) , tal y como lo dicta uno de estos argumentos [EndDialog](enddialog-controlevent.md) asociados al botón insertado por el usuario:

**Reintentar**: se borran todos los valores agregados a la tabla de [cuadro de lista](listbox-table.md) y se repite todo el procedimiento de [*costo*](c-gly.md) de archivos, con lo que se vuelve a comprobar los archivos que todavía están en uso. Si todavía se identifican uno o más procesos como el uso de archivos que se van a sobrescribir o eliminar, el proceso se repite; de lo contrario, InstallValidate devuelve el control al instalador con un estado de msiDoActionStatusSuccess.

**Exit**: la acción InstallValidate devuelve inmediatamente el control al instalador con un estado de msiDoActionStatusUserExit. Esto finaliza la instalación.

**Cualquier otro valor devuelto**: la acción InstallValidate devuelve inmediatamente el control al instalador con un estado de msiDoActionStatusSuccess. En este caso, como uno o varios archivos todavía están en uso, las siguientes acciones de [InstallFiles](installfiles-action.md) y/o [InstallAdminPackage](installadminpackage-action.md) deben programar los archivos en uso que se van a reemplazar o eliminar cuando se reinicie el sistema.

Si no hay ninguna tabla [ListBox](listbox-table.md) en la base de datos, InstallValidate se cierra silenciosamente sin un error.

El punto y coma es el delimitador de lista para las transformaciones, los orígenes y las revisiones, y no debe usarse en estos nombres de archivo o rutas de acceso.

Los archivos marcados como de solo lectura en una ubicación de solo lectura nunca se consideran utilizados por el instalador.

Si el nivel de la interfaz de usuario es básico, se presenta al usuario un cuadro **de diálogo de espacio en disco** predeterminado que contiene los botones **anular** y **Reintentar** .

 

 



