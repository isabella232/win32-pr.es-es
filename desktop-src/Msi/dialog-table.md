---
description: La tabla de diálogos contiene todos los diálogos que aparecen en la interfaz de usuario (UI) en los modos completo y reducido.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Tabla de diálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554bc551b41a7ebeaa8b63b2a0d1b74a0f55cfb1d7a087936a394a060286caba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692845"
---
# <a name="dialog-table"></a>Tabla de diálogos

La tabla de diálogos contiene todos los diálogos que aparecen en la interfaz de usuario (UI) en los modos completo y reducido.

La tabla dialog tiene las siguientes columnas.



| Columna           | Tipo                               | Clave | Nullable |
|------------------|------------------------------------|-----|----------|
| Diálogo           | [Identificador](identifier.md)       | Y   | N        |
| HCentering       | [Entero](integer.md)             | N   | N        |
| VCentering       | [Entero](integer.md)             | N   | N        |
| Ancho            | [Entero](integer.md)             | N   | N        |
| Alto           | [Entero](integer.md)             | N   | N        |
| Atributos       | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Título            | [Formato](formatted.md)         | N   | Y        |
| Control \_ First   | [Identificador](identifier.md)       | N   | N        |
| Control \_ predeterminado | [Identificador](identifier.md)       | N   | Y        |
| Cancelar \_ control  | [Identificador](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Diálogo
</dt> <dd>

Clave principal y nombre del cuadro de diálogo.

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

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altura
</dt> <dd>

Alto del límite rectangular del cuadro de diálogo.

Este número no debe ser negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Palabra de 32 bits que especifica las marcas de atributo que se aplicarán a este cuadro de diálogo.

Este número no debe ser negativo. Para obtener más información, vea [Bits de estilo de diálogo](dialog-style-bits.md).

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Cadena de texto localizable que especifica el título que se va a mostrar en la barra de título del cuadro de diálogo.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Control \_ First
</dt> <dd>

Clave externa a la segunda columna de la [tabla de control](control-table.md).

La combinación de este campo con el campo [](control-table.md) Diálogo especifica un control único en la tabla de control que toma el foco cuando se abre el cuadro de diálogo. Normalmente, puede ser un [control Edit Control](edit-control.md), [SelectionTree Control](selectiontree-control.md)o cualquier otro control que pueda tomar el foco. Si el [control PushButton](pushbutton-control.md) es el único control presente en el cuadro de diálogo que puede tomar el foco, el elemento PushButton especificado en el campo ControlDefault también debe especificarse en el campo Control First. Esta columna se omite en un cuadro [de diálogo Error.](error-dialog.md)

Dado que el texto estático no puede tomar el foco, un [control](text-control.md) de texto que describe un control De edición [,](edit-control.md) [PathEdit Control](pathedit-control.md), [ListView Control](listview-control.md), [ComboBox Control](combobox-control.md) o [VolumeSelectCombo Control](volumeselectcombo-control.md) debe ser el primer control en el cuadro de diálogo para garantizar la compatibilidad con los lectores de pantalla.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Control \_ predeterminado
</dt> <dd>

Clave externa a la segunda columna de la [tabla de control](control-table.md).

La combinación de este campo con el campo Diálogo especifica el control predeterminado que toma el foco cuando se abre el cuadro de diálogo. Normalmente, puede ser un [control PushButton](pushbutton-control.md). Si ningún control PushButton del cuadro de diálogo tiene el foco, la tecla Devolver equivale a hacer clic en el control predeterminado. Si esta columna se deja en blanco, no hay ningún control predeterminado. Esta columna se omite en un cuadro [de diálogo Error.](error-dialog.md)

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Cancelar \_ control
</dt> <dd>

Clave externa a la segunda columna de la [tabla de control](control-table.md).

La combinación de este campo con el campo Diálogo especifica un control que cancela la instalación. Este control se acopla a los eventos de la [tabla ControlEvent que](controlevent-table.md) se usa para cancelar la instalación. Pulsar la tecla ESC o hacer clic en el botón Cerrar equivale a hacer clic en el control cancelar. Esta columna se omite en un cuadro [de diálogo de error](error-dialog.md)

.

El control de cancelación se oculta durante la reversión o la eliminación de archivos de copia de seguridad. El controlador interno de la interfaz de usuario oculta el control al recibir un mensaje INSTALLMESSAGE \_ COMMONDATA.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los valores enteros de ancho y alto están en las unidades [del instalador,](installer-units.md)no en las unidades de diálogo.

Los dos valores de centrado se omiten para los cuadros de diálogo posteriores de una secuencia del asistente. Las posiciones del cuadro de diálogo las establece el usuario o como para el cuadro de diálogo anterior. Estas secuencias de cuadro de diálogo se crean mediante [un objeto NewDialog ControlEvent](newdialog-controlevent.md).

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

 

 



