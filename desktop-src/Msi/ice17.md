---
description: ICE17 comprueba las situaciones que se muestran en el ejemplo al final de este tema.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c296273e1de5ae633b2708c92cf0376018e6d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910918"
---
# <a name="ice17"></a>ICE17

ICE17 comprueba las situaciones que se muestran en el ejemplo al final de este tema.

## <a name="result"></a>Resultado

ICE17 muestra un mensaje de error o advertencia para cada una de las situaciones en el ejemplo. En la tabla siguiente se muestran ejemplos de estos mensajes.



| Error o advertencia de ICE17                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PushButton: button1 del cuadro de diálogo: el cuadro de diálogo no tiene un evento definido en la tabla ControlEvent,. Error <br/>                                                                                                                | Hay un [control Pushbutton](pushbutton-control.md) que no se muestra en la [tabla ControlEvent,](controlevent-table.md). Si ICE17 devuelve este error en un control de acceso para el que no se ha establecido el atributo **enable control** o el atributo **control visible** en la columna Attributes de la [tabla de control](control-table.md), compruebe si el control también tiene una entrada en la [tabla ControlCondition](controlcondition-table.md). El control se puede habilitar de manera inesperada, o visible, si el valor de la columna Condition cambia a true, enable o show.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: Bitmap1 de control: Bitmap1 del cuadro de diálogo: el cuadro de diálogo no está en la tabla binaria. Error <br/>                                                                                                                              | Hay un control de [mapa de bits](bitmap-control.md) o un control de [icono](icon-control.md), pero el mapa de bits o el icono correspondiente no aparece en la [tabla binaria](binary-table.md). Agregue el mapa de bits o el icono a la tabla binaria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 del control: RadioButton1 del cuadro de diálogo: el cuadro de diálogo no está en la tabla RadioButton. Advertencia <br/>                                                                                                   | Hay un [control RadioButtonGroup](radiobuttongroup-control.md) con valores en la columna propiedad y la columna atributo de la [tabla de control](control-table.md). el bit [indirecto](indirect-control-attribute.md) no se establece en la columna Attributes. ICE17 publica una advertencia porque el instalador usa el valor de la propiedad como una clave externa en la tabla RadioButton, pero el valor no se encuentra en la clave principal de esa tabla. Si se establece el bit [indirecto](indirect-control-attribute.md) , la propiedad enumerada para el control no se utiliza como la propiedad; en su lugar, se utiliza como el nombre de la propiedad que se usa realmente.<br/> Esta advertencia se puede pasar por alto si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) de en el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/> |
| ListBox: ListBox1 de control: ListBox1 del cuadro de diálogo: el cuadro de diálogo no está en la tabla ListBox. Advertencia <br/>                                                                                                                        | Hay un [control ListBox](listbox-control.md) con un valor en la columna Property de la [tabla de control](control-table.md) y para el que no se establece el bit [indirecto](indirect-control-attribute.md) en la columna Attributes. ICE17 publica una advertencia porque el instalador usa el valor de la propiedad como una clave externa en la [tabla de cuadro de lista](listbox-table.md), pero falta el valor de la clave principal de esa tabla. Si se establece el bit [indirecto](indirect-control-attribute.md) , el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede pasar por alto si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) de en el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                                |
| ComboBox: ComboBox1 del control: ComboBox1 del cuadro de diálogo: ByDialog no está en la advertencia de la tabla ComboBox <br/>                                                                                                                     | Hay un [control ComboBox](combobox-control.md) con un valor en la columna de propiedades de la [tabla de control](control-table.md) y para el que no se establece el bit [indirecto](indirect-control-attribute.md) en la columna Attributes. ICE17 publica una advertencia porque el instalador usa el valor de la propiedad como una clave externa en la [tabla de cuadro combinado](combobox-table.md), pero el valor no se encuentra en la clave principal de esa tabla. Si se establece el bit [indirecto](indirect-control-attribute.md) , el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede pasar por alto si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) de en el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                            |
| ListView: ListView1 del control: ListView1 del cuadro de diálogo: mi cuadro de diálogo no está en la tabla ListView. Advertencia <br/>                                                                                                                    | Hay un [control ListView](listview-control.md) con un valor en la columna de propiedades de la [tabla de control](control-table.md) y para el que no se establece el bit [indirecto](indirect-control-attribute.md) en la columna Attributes. ICE17 publica una advertencia porque el instalador usa el valor de la propiedad como una clave externa en la [tabla ListView](listview-table.md), pero falta el valor de la clave principal de esa tabla. Si se establece el bit [indirecto](indirect-control-attribute.md) , el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede pasar por alto si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) de en el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                            |
| Mapa de bits: ' Bitmap2 ' para el control: ' BUTTON2 ' del cuadro de diálogo: ' no se encuentra el cuadro de diálogo ' en el error de tabla binaria <br/>                                                                                                                         | Hay un control [Pushbutton](pushbutton-control.md) o un [control CheckBox](checkbox-control.md) para el que la columna de texto de la [tabla de control](control-table.md) no contiene una clave externa en el registro de la [tabla binaria](binary-table.md) que contiene el mapa de bits o el icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Mapa de bits: ' Bitmap3 ' para el control: ' RadioButton2 ' del cuadro de diálogo: ' no se encuentra el cuadro de diálogo ' en la tabla binaria o<br/> Icono: ' Icon1 ' para el control: ' RadioButton3 ' del cuadro de diálogo: ' no se encuentra el cuadro de diálogo ' en la tabla binaria<br/> Error <br/> | Hay un [control RadioButtonGroup](radiobuttongroup-control.md) para el que la columna de texto de la [tabla RadioButton](radiobutton-table.md) no contiene una clave externa en el registro de la [tabla binaria](binary-table.md) que contiene el mapa de bits o el icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Control de imagen: ' button3 ' del cuadro de diálogo: ' mi diálogo ' tiene los atributos de icono y de mapa de bits Set error <br/>                                                                                                                     | Hay un control [Pushbutton](pushbutton-control.md), [CheckBox](checkbox-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) con el bit de [icono](icon-control-attribute.md) o el bit de [mapa](bitmap-control-attribute.md) de bits establecido en la columna Attributes de la tabla de [control](control-table.md). No se pueden establecer ambos atributos juntos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Ejemplo

[Tabla de control](control-table.md) (parcial)



| Diálogo\_ | Control      | Tipo             | Atributos | Propiedad     | Texto       |
|----------|--------------|------------------|------------|--------------|------------|
| Cuadro de diálogo | Button1      | Botones       | 0          |              | Aceptar         |
| Cuadro de diálogo | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| Cuadro de diálogo | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| Cuadro de diálogo | Cuadrolista1     | ListBox          | 0          | Cuadrolista1     |            |
| Cuadro de diálogo | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| Cuadro de diálogo | ListView1    | ListView         | 0          | ListView1    |            |
| Cuadro de diálogo | Button2      | Botones       | 262 144     |              | Bitmap2    |
| Cuadro de diálogo | RadioButton2 | RadioButtonGroup | 262 144     |              | Property2  |
| Cuadro de diálogo | RadioButton3 | RadioButtonGroup | 524 288     |              | Property3  |
| Cuadro de diálogo | Button3      | Botones       | 786432     |              | Ambiguous1 |



 

[Tabla RadioButton](radiobutton-table.md) (parcial)



| Propiedad\_ | Pedido | Texto    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

Las tablas siguientes están vacías:

-   [Tabla ControlEvent,](controlevent-table.md)
-   [Tabla ListBox](listbox-table.md)
-   [Tabla ComboBox](combobox-table.md)
-   [Tabla ListView](listview-table.md)
-   [Tabla binaria](binary-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




