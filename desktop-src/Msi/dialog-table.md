---
description: La tabla cuadro de diálogo contiene todos los cuadros de diálogo que aparecen en la interfaz de usuario (UI) en los modos completo y reducido.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Tabla de cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a210ad051eec950dcff8f8f940a1df11bf74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910958"
---
# <a name="dialog-table"></a>Tabla de cuadro de diálogo

La tabla cuadro de diálogo contiene todos los cuadros de diálogo que aparecen en la interfaz de usuario (UI) en los modos completo y reducido.

La tabla del cuadro de diálogo tiene las columnas siguientes.



| Columna           | Tipo                               | Clave | Nullable |
|------------------|------------------------------------|-----|----------|
| Diálogo           | [Identificador](identifier.md)       | Y   | N        |
| HCentering       | [Entero](integer.md)             | N   | N        |
| VCentering       | [Entero](integer.md)             | N   | N        |
| Ancho            | [Entero](integer.md)             | N   | N        |
| Alto           | [Entero](integer.md)             | N   | N        |
| Atributos       | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Title            | [Formatea](formatted.md)         | N   | Y        |
| Controlar \_ primero   | [Identificador](identifier.md)       | N   | N        |
| \_Valor predeterminado del control | [Identificador](identifier.md)       | N   | Y        |
| \_Cancelar control  | [Identificador](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Diálogo
</dt> <dd>

La clave principal y el nombre del cuadro de diálogo.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

Posición horizontal del cuadro de diálogo.

El intervalo es de 0 a 100, con 0 en el borde izquierdo de la pantalla y 100 en el borde derecho.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

Posición vertical del cuadro de diálogo.

El intervalo es de 0 a 100, con 0 en el borde superior de la pantalla y 100 en el borde inferior.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Ancho
</dt> <dd>

Ancho del límite rectangular del cuadro de diálogo.

Este número no debe ser negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Alto
</dt> <dd>

Alto del límite rectangular del cuadro de diálogo.

Este número no debe ser negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Palabra de 32 bits que especifica las marcas de atributo que se van a aplicar a este cuadro de diálogo.

Este número no debe ser negativo. Para obtener más información, vea [bits de estilo de cuadro de diálogo](dialog-style-bits.md).

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titulo
</dt> <dd>

Cadena de texto traducible que especifica el título que se va a mostrar en la barra de título del cuadro de diálogo.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Controlar \_ primero
</dt> <dd>

Una clave externa a la segunda columna de la [tabla de control](control-table.md).

La combinación de este campo con el campo de cuadro de diálogo especifica un control único en la [tabla de control](control-table.md) que toma el foco cuando se abre el cuadro de diálogo. Normalmente, puede ser un control de [edición](edit-control.md), un [control SelectionTree](selectiontree-control.md)o cualquier otro control que pueda tomar el foco. Si el [control Pushbutton](pushbutton-control.md) es el único control presente en el cuadro de diálogo que puede tomar el foco, el control de pulsador especificado en el campo ControlDefault también se debe escribir en el primer campo del control. Esta columna se omite en un cuadro de [diálogo de error](error-dialog.md) .

Dado que el texto estático no puede tomar el foco, un [control de texto](text-control.md) que describe un control de [edición](edit-control.md), [PathEdit](pathedit-control.md), control de [ListView](listview-control.md), control [ComboBox](combobox-control.md) o [control VolumeSelectCombo](volumeselectcombo-control.md) debe ser el primer control del cuadro de diálogo para garantizar la compatibilidad con los lectores de pantalla.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>\_Valor predeterminado del control
</dt> <dd>

Una clave externa a la segunda columna de la [tabla de control](control-table.md).

Al combinar este campo con el campo del cuadro de diálogo, se especifica el control predeterminado que toma el foco al abrir el cuadro de diálogo. Normalmente, puede ser un [control Pushbutton](pushbutton-control.md). Si no hay ningún control de pulsador en el cuadro de diálogo que tenga el foco, la tecla devuelta es equivalente a hacer clic en el control predeterminado. Si esta columna se deja en blanco, no hay ningún control predeterminado. Esta columna se omite en un cuadro de [diálogo de error](error-dialog.md) .

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>\_Cancelar control
</dt> <dd>

Una clave externa a la segunda columna de la [tabla de control](control-table.md).

Al combinar este campo con el campo del cuadro de diálogo, se especifica un control que cancela la instalación. Este control se asocia a los eventos de la [tabla ControlEvent,](controlevent-table.md) que se usa para cancelar la instalación. Presionar la tecla ESC o hacer clic en el botón Cerrar es equivalente a hacer clic en el control cancelar. Esta columna se omite en un [cuadro de diálogo de error](error-dialog.md)

.

El control cancelar está oculto durante la reversión o la eliminación de los archivos de los que se ha realizado una copia de seguridad. El controlador de interfaz de usuario interno oculta el control al recibir un \_ mensaje COMMONDATA de INSTALLMESSAGE.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores enteros para el ancho y el alto se encuentran en las [unidades de instalador](installer-units.md), no en las unidades de cuadro de diálogo.

Los dos valores de centrado se omiten en los cuadros de diálogo posteriores en una secuencia de asistente. Las posiciones del cuadro de diálogo las establece el usuario o como para el cuadro de diálogo anterior. Estas secuencias de cuadro de diálogo se crean mediante un [ControlEvent, NewDialog](newdialog-controlevent.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



