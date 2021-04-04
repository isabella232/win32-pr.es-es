---
description: En la tabla EventMapping se muestran los controles que se suscriben a algunos eventos de control y se enumera el atributo que se va a cambiar cuando otro control o el Windows Installer publiquen el evento.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabla EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908857"
---
# <a name="eventmapping-table"></a>Tabla EventMapping

En la tabla EventMapping se muestran los controles que se suscriben a algunos eventos de control y se enumera el atributo que se va a cambiar cuando otro control o el Windows Installer publiquen el evento.

La tabla EventMapping tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Diálogo\_  | [Identificador](identifier.md) | Y   | N        |
| control\_ | [Identificador](identifier.md) | Y   | N        |
| Evento     | [Identificador](identifier.md) | Y   | N        |
| Atributo | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_
</dt> <dd>

Una clave externa a la primera columna de la [tabla del cuadro de diálogo](dialog-table.md). Este campo y el campo de control \_ identifican un control.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_
</dt> <dd>

Una clave externa a la segunda columna de la [tabla de control](control-table.md). Este campo y el campo de diálogo \_ juntos identifican un control.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso
</dt> <dd>

Este campo es un identificador que especifica el tipo de evento al que se suscribe el control. Para obtener más información, consulte [información general de ControlEvent,](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui
</dt> <dd>

Nombre del atributo de control \_ que se establece cuando se recibe el evento en la columna de evento. El argumento del evento se pasa como argumento de la llamada de atributo para cambiar este atributo del control.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [tabla ControlEvent,](controlevent-table.md) especifica los eventos de control que se inician cuando un usuario interactúa con un control [Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Estos son los únicos controles que un usuario puede usar para iniciar eventos de control.

Hay más de un control en un cuadro de diálogo que se puede suscribir al mismo evento.

En la lista siguiente se identifican los usos típicos de la tabla EventMapping:

-   Para suscribir [un control de texto](text-control.md) a un ControlEvent, de [ActionText](actiontext-controlevent.md), [ActionData ControlEvent,](actiondata-controlevent.md), [ScriptInProgress controlevent,](scriptinprogress-controlevent.md) o [TimeRemaining ControlEvent,](timeremaining-controlevent.md) publicado por el Windows Installer.
-   Para suscribir un control [ProgressBar](progressbar-control.md) o un control de la [cartelera](billboard-control.md) a un [ControlEvent, de SetProgress](setprogress-controlevent.md).
-   Para suscribir un [control DirectoryCombo](directorycombo-control.md) a un [ControlEvent, de IgnoreChange](ignorechange-controlevent.md).
-   Para deshabilitar automáticamente un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo con un [control SelectionTree](selectiontree-control.md). Para deshabilitar el botón de control cuando no aparezca ninguna característica en el [control SelectionTree](selectiontree-control.md), use la tabla EventMapping para suscribir el control Pushbutton a un [SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md). Escriba **enable** en el campo Attributes de la tabla EventMapping.
-   Para mostrar un [control de texto](text-control.md) que muestra la ruta de acceso a la ubicación de instalación de la característica seleccionada en un [control SelectionTree](selectiontree-control.md) en el mismo cuadro de diálogo. Use la tabla EventMapping para suscribir [el control de texto](text-control.md) a [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) y [SelectionPath ControlEvent,](selectionpath-controlevent.md) publicado por el [control SelectionTree](selectiontree-control.md).
-   Para mostrar un [control de texto](text-control.md) que muestre una descripción del elemento resaltado en un [control SelectionTree](selectiontree-control.md) ubicado en el mismo cuadro de diálogo, use la tabla EventMapping para suscribir el [control de texto](text-control.md) a [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [SelectionSize ControlEvent,](selectionsize-controlevent.md) o [SelectionAction ControlEvent,](selectionaction-controlevent.md). Escriba el **texto** en el campo atributo de la tabla EventMapping.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



