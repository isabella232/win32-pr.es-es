---
description: La tabla ControlEvent permite al autor especificar los eventos de control iniciados cuando un usuario interactúa con un control PushButton, un control CheckBox o un control SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabla ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158768"
---
# <a name="controlevent-table"></a>Tabla ControlEvent

La tabla ControlEvent permite al autor especificar los eventos [de control](control-events.md) iniciados cuando un usuario interactúa con un [control PushButton,](pushbutton-control.md) [un control CheckBox](checkbox-control.md)o [un control SelectionTree](selectiontree-control.md). Estos son los únicos controles que los usuarios pueden usar para iniciar eventos de control. Cada control puede publicar varios eventos de control. El instalador inicia cada evento en el orden especificado en la columna Ordering . Por ejemplo, un control de botón de inserción puede publicar eventos para iniciar una transición a otro cuadro de diálogo, salir de la secuencia del cuadro de diálogo y comenzar la instalación de archivos.

La excepción que se debe tener en cuenta es que cada control puede publicar un evento [NewDialog](newdialog-controlevent.md) o [SpawnDialog](spawndialog-controlevent.md) como máximo. Si necesita crear varios eventos de control NewDialog y SpawnDialog en esta tabla, incluya también instrucciones condicionales en los campos Condición que garanticen que como máximo se publica un evento. Si se seleccionan varios eventos de control NewDialog y SpawnDialog para el mismo control, solo se publica el evento con el valor más grande de la columna Ordering cuando se activa el control.

La tabla ControlEvent tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Diálogo\_  | [Identificador](identifier.md) | Y   | N        |
| control\_ | [Identificador](identifier.md) | Y   | N        |
| Evento     | [Formato](formatted.md)   | Y   | N        |
| Argumento  | [Formato](formatted.md)   | Y   | N        |
| Condición | [Condition](condition.md)   | Y   | Y        |
| Ordenación  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_
</dt> <dd>

Clave externa de la primera columna de la tabla [Dialog](dialog-table.md). La combinación de este campo con el campo Control \_ identifica un control único.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_
</dt> <dd>

Clave externa de la segunda columna de la [tabla Control](control-table.md). La combinación de este campo con el campo \_ Diálogo identifica un control único.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Identificador que especifica el tipo de evento que debe tener lugar cuando el usuario interactúa con el control especificado por Dialog \_ y Control \_ . Para obtener una lista de valores posibles, [vea Información general de ControlEvent.](controlevent-overview.md)

Para establecer una propiedad con un control , coloque Nombre de propiedad en este campo y \[ el nuevo valor en el campo de \_ \] argumento. Coloque { } en el campo de argumento para escribir el valor NULL.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Valor que se usa como modificador al desencadenar un evento determinado.

Por ejemplo, el argumento de [NewDialog ControlEvent](newdialog-controlevent.md) o [SpawnDialog ControlEvent](spawndialog-controlevent.md) es el nombre del cuadro de diálogo y el argumento de la acción [Install](install-action.md) es un número que define el nivel de instalación.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Instrucción condicional que determina si el instalador activa el evento en la columna Evento . El instalador desencadena el evento si la instrucción condicional del campo Condición se evalúa como True. Por lo tanto, coloque un 1 en esta columna para asegurarse de que el instalador desencadena el evento . El instalador no desencadena el evento si el campo Condición contiene una instrucción que se evalúa como False. El instalador no desencadena un evento con un espacio en blanco en el campo Condición a menos que ningún otro evento del control se evalúe como True. Si ninguno de los campos Condición del control denominado en el campo Control se evalúa como True, el instalador desencadena el evento que tiene un campo Condición en blanco y, si hay más de un campo Condición en blanco, se desencadena el único evento de estos con el valor más grande en el \_ campo Ordenación. Vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenar
</dt> <dd>

Entero que se usa para ordenar varios eventos asociados al mismo control. Debe ser un número no negativo. Este campo se puede dejar en blanco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En [la tabla EventMapping](eventmapping-table.md) se enumeran los controles que se suscriben a algún evento de control y se muestra el atributo de control que se va a cambiar cuando el otro control o el instalador publique ese evento.

En Windows XP o sistemas operativos anteriores, los usuarios pueden publicar un evento de control solo mediante la interacción con un [control de](checkbox-control.md) casilla o un control de botón [de inserción](pushbutton-control.md). Con Windows Server 2003, los usuarios pueden publicar un evento de control solo mediante la interacción con un [control Checkbox](checkbox-control.md), [SelectionTree Control](selectiontree-control.md)y [pushbutton Control](pushbutton-control.md). Enumerar otros controles en el campo \_ Control no tiene ningún efecto.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



