---
description: ICE17 comprueba las situaciones que se muestran en el ejemplo al final de este tema.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e9714edebd666173a82c75fc6e8fed54a511c64adaa387013648b2f190e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529205"
---
# <a name="ice17"></a>ICE17

ICE17 comprueba las situaciones que se muestran en el ejemplo al final de este tema.

## <a name="result"></a>Resultado

ICE17 muestra un mensaje de error o advertencia para cada una de las situaciones del ejemplo. En la tabla siguiente se muestran ejemplos de estos mensajes.



| Error o advertencia de ICE17                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PushButton: Button1 de Dialog: MyDialog no tiene un evento definido en la tabla ControlEvent. Error <br/>                                                                                                                | Hay un control [Pushbutton que](pushbutton-control.md) no aparece en la [tabla ControlEvent](controlevent-table.md). Si ICE17 devuelve este error en un elemento PushButton para el que el atributo **Enable Control** o el atributo Visible **Control** no están establecidos en la columna Atributos de la tabla [Control](control-table.md), compruebe si el control también tiene una entrada en la [tabla ControlCondition](controlcondition-table.md). El control puede habilitarse o verse de forma inesperada si el valor de la columna Condición cambia a True, Enable o Show.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: Bitmap1 of Control: Bitmap1 of Dialog: MyDialog is not in the Binary table. Error <br/>                                                                                                                              | Hay un control [Bitmap o](bitmap-control.md) un [control Icon](icon-control.md), pero el mapa de bits o icono correspondiente no aparece en la [tabla binaria](binary-table.md). Agregue el mapa de bits o el icono a la tabla Binaria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 de Control: RadioButton1 de Dialog: MyDialog no está en la tabla RadioButton. Advertencia <br/>                                                                                                   | Hay un control [RadioButtonGroup con](radiobuttongroup-control.md) valores en la columna Property y en la columna Attribute de la [tabla Control](control-table.md). El [bit](indirect-control-attribute.md) indirecto no se establece en la columna Atributos. ICE17 envía una advertencia porque el instalador usa el valor de la propiedad como clave externa en la tabla RadioButton, pero falta el valor de la clave principal de esa tabla. Si se [establece el](indirect-control-attribute.md) bit indirecto, la propiedad enumerada para el control no se usa como propiedad; en su lugar, se usa como el nombre de la propiedad que se usa realmente.<br/> Esta advertencia se puede omitir si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) para en el cuadro de diálogo [FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/> |
| ListBox: ListBox1 de Control: ListBox1 de Dialog: MyDialog no está en la tabla ListBox. Advertencia <br/>                                                                                                                        | Hay un [control ListBox](listbox-control.md) con un valor en la columna Propiedad de la [tabla Control](control-table.md) y para el que el bit indirecto no está establecido en la columna Atributos. [](indirect-control-attribute.md) ICE17 envía una advertencia porque el instalador usa el valor de la propiedad como clave externa en la tabla [ListBox](listbox-table.md), pero falta el valor de la clave principal de esa tabla. Si se [establece el](indirect-control-attribute.md) bit indirecto, el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede omitir si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) para en el cuadro de diálogo [FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                                |
| ComboBox: ComboBox1 of Control: ComboBox1 of Dialog: ByDialog is not in the ComboBox table Warning <br/>                                                                                                                     | Hay un [control ComboBox con](combobox-control.md) un valor en la columna Propiedad de la tabla [Control](control-table.md) y para el que el [bit](indirect-control-attribute.md) indirecto no está establecido en la columna Atributos. ICE17 envía una advertencia porque el instalador usa el valor de la propiedad como clave externa en la tabla [ComboBox](combobox-table.md), pero falta el valor de la clave principal de esa tabla. Si se [establece el](indirect-control-attribute.md) bit indirecto, el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede omitir si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) para en el cuadro de diálogo [FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                            |
| ListView: ListView1 of Control: ListView1 of Dialog: MyDialog is not in the ListView table. Advertencia <br/>                                                                                                                    | Hay un [control ListView](listview-control.md) con un valor en la columna Property de la [tabla Control](control-table.md) y para el que el bit indirecto no está establecido en la columna Atributos. [](indirect-control-attribute.md) ICE17 envía una advertencia porque el instalador usa el valor de la propiedad como clave externa en la tabla [ListView](listview-table.md), pero falta el valor de la clave principal de esa tabla. Si se [establece el](indirect-control-attribute.md) bit indirecto, el control cambia el valor de una propiedad que tiene un nombre que es el valor de la propiedad asociada a este control.<br/> Esta advertencia se puede omitir si el control se crea en tiempo de ejecución. Por ejemplo, el [control ListBox](listbox-control.md) para en el cuadro de diálogo [FilesInUse](filesinuse-dialog.md) solo se crea en tiempo de ejecución si hay archivos en uso durante la instalación.<br/>                            |
| Bitmap: 'Bitmap2' for Control: 'Button2' of Dialog: 'MyDialog' not found in Binary table Error <br/>                                                                                                                         | Hay un control [Control](pushbutton-control.md) de botón de inserción o [control](checkbox-control.md) de casilla para el que la columna Texto de la [tabla Control](control-table.md) no contiene una clave externa en el registro de la tabla [Binaria](binary-table.md) que contiene el mapa de bits o el icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: 'Bitmap3' for Control: 'RadioButton2' of Dialog: 'MyDialog' not found in Binary table or<br/> Icono: 'Icon1' para Control: 'RadioButton3' del cuadro de diálogo: 'MyDialog' no se encuentra en la tabla binaria<br/> Error <br/> | Hay un [control RadioButtonGroup](radiobuttongroup-control.md) para el que la columna Text de la tabla [RadioButton](radiobutton-table.md) no contiene una clave externa en el registro de la tabla [Binary](binary-table.md) que contiene el mapa de bits o el icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Control Imagen: 'Button3' del cuadro de diálogo: 'MyDialog' tiene los atributos Icon y Bitmap establecidos en Error <br/>                                                                                                                     | Hay un control [PushButton,](pushbutton-control.md) [CheckBox](checkbox-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) con el bit [icon](icon-control-attribute.md) o [bitmap](bitmap-control-attribute.md) establecido en la columna Attributes de la [tabla Control](control-table.md). No se pueden establecer ambos atributos juntos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Ejemplo

[Tabla de control](control-table.md) (parcial)



| Diálogo\_ | Control      | Tipo             | Atributos | Propiedad     | Texto       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | Pulsador       | 0          |              | Aceptar         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | Pulsador       | 262 144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262 144     |              | Propiedad 2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524 288     |              | Propiedad 3  |
| MyDialog | Button3      | Pulsador       | 786432     |              | Ambiguous1 |



 

[Tabla RadioButton](radiobutton-table.md) (parcial)



| Propiedad\_ | Pedido | Texto    |
|------------|-------|---------|
| Propiedad 2  | 1     | Bitmap3 |
| Propiedad 3  | 2     | Icono1   |



 

Las tablas siguientes están vacías:

-   [Tabla ControlEvent](controlevent-table.md)
-   [ListBox Table](listbox-table.md)
-   [Tabla ComboBox](combobox-table.md)
-   [ListView (tabla)](listview-table.md)
-   [Tabla binaria](binary-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




