---
title: Elemento ControlGroup
description: Representa un grupo de controles en una plantilla de diseño SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- ControlGroup, elemento Windows cinta de opciones
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33640f8e451f7124efda8c0e5377a3145d221668
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631993"
---
# <a name="controlgroup-element"></a>Elemento ControlGroup

Representa un grupo de controles en una [**plantilla de diseño SizeDefinition.**](windowsribbon-element-sizedefinition.md)

## <a name="usage"></a>Uso

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Válido solo cuando <a href="windowsribbon-element-group.md"><strong>Group</strong></a> es el elemento primario.<br/> Cada <em>SequenceNumber</em> debe ser único dentro de un <a href="windowsribbon-element-group.md"><strong>elemento Group.</strong></a> Los valores de <em>SequenceNumber</em> deben aumentar para cada <strong>elemento Group,</strong> pero no es necesario que sean secuenciales. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo entre 1000 y 59999, ambos incluidos.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                 | Descripción                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                               | Puede producirse una o varias veces<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Puede producirse una o varias veces<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Puede producirse como máximo una vez<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>             | Puede producirse una o varias veces<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                             |
|-------------------------------------------------------------------------------------|
| **ControlGroup**<br/>                                                         |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                             |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Fila**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para cada [**elemento Group**](windowsribbon-element-group.md) **o ControlGroup.**

Si no se proporcionan números de secuencia, los elementos se representan en el orden especificado en el marcado de la cinta de opciones.

Si [**Group**](windowsribbon-element-group.md) o **ControlGroup** es el elemento primario, **ControlGroup** se restringe a los siguientes elementos secundarios posibles: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md)

De lo contrario, [**cuando Row**](windowsribbon-element-row.md) o [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) es el elemento primario, [**Group**](windowsribbon-element-group.md) está restringido al siguiente elemento secundario posible: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado básico para una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con varios [**elementos Group.**](windowsribbon-element-group.md)


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





