---
description: La tabla EventMapping enumera los controles que se suscriben a algunos eventos de control y muestra el atributo que se va a cambiar cuando otro control o el instalador de Windows publica el evento.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabla EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158441"
---
# <a name="eventmapping-table"></a>Tabla EventMapping

La tabla EventMapping enumera los controles que se suscriben a algunos eventos de control y muestra el atributo que se va a cambiar cuando otro control o el instalador de Windows publica el evento.

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

Clave externa de la primera columna de la tabla [de diálogos](dialog-table.md). Este campo y el campo Control \_ identifican juntos un control.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_
</dt> <dd>

Clave externa a la segunda columna de la [tabla de control](control-table.md). Este campo y el campo Diálogo \_ juntos identifican un control.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Este campo es un identificador que especifica el tipo de evento al que está suscrito el control . Para obtener más información, vea [Información general de ControlEvent.](controlevent-overview.md)

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atributo
</dt> <dd>

Nombre del atributo Control \_ que se establece cuando se recibe el evento de la columna Evento. El argumento del evento se pasa como argumento de la llamada de atributo para cambiar este atributo del control.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [tabla ControlEvent especifica](controlevent-table.md) los eventos de control que se inician cuando un usuario interactúa con un control [PushButton](pushbutton-control.md), un control [CheckBox](checkbox-control.md)o [un control SelectionTree](selectiontree-control.md). Estos son los únicos controles que un usuario puede usar para iniciar eventos de control.

Más de un control de un cuadro de diálogo puede suscribirse al mismo evento.

En la lista siguiente se identifican los usos típicos de la tabla EventMapping:

-   Para suscribir un [control de](text-control.md) texto a un [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) o [TimeRemaining ControlEvent](timeremaining-controlevent.md) publicado por el instalador Windows.
-   Para suscribir un [control ProgressBar o](progressbar-control.md) [Un control Descontrol a](billboard-control.md) un control [SetProgress ControlEvent](setprogress-controlevent.md).
-   Para suscribir un [control DirectoryCombo a](directorycombo-control.md) [un control IgnoreChange ControlEvent](ignorechange-controlevent.md).
-   Para deshabilitar automáticamente un control [PushButton ubicado](pushbutton-control.md) en el mismo cuadro de diálogo con un [control SelectionTree](selectiontree-control.md). Para deshabilitar el botón de inserción cuando no aparece ninguna característica en el [control SelectionTree](selectiontree-control.md), use la tabla EventMapping para suscribir el control PushButton a [un control SelectionNoItems ControlEvent](selectionnoitems-controlevent.md). Escriba **Habilitar** en el campo Atributos de la tabla EventMapping.
-   Para mostrar un [control de texto que](text-control.md) muestra la ruta de acceso a la ubicación de instalación de la característica seleccionada en un control [SelectionTree en](selectiontree-control.md) el mismo cuadro de diálogo. Use la tabla EventMapping para suscribir el [control](text-control.md) de texto a [un control SelectionPathOn ControlEvent](selectionpathon-controlevent.md) y [SelectionPath ControlEvent](selectionpath-controlevent.md) publicado por el [control SelectionTree](selectiontree-control.md).
-   Para mostrar un [control](text-control.md) de texto que muestra una descripción del elemento resaltado en un [control SelectionTree](selectiontree-control.md) ubicado en el mismo cuadro de diálogo, use la tabla EventMapping para suscribir el [control](text-control.md) de texto a un control [SelectionDescription ControlEvent,](selectiondescription-controlevent.md) [SelectionSize ControlEvent](selectionsize-controlevent.md) o [SelectionAction ControlEvent](selectionaction-controlevent.md). Escriba **Texto** en el campo Atributo de la tabla EventMapping.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



