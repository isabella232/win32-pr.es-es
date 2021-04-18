---
title: Elemento GroupSizeDefinition
description: Representa un tamaño de diseño de un grupo de controles en una plantilla personalizada.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition cinta de opciones de Windows
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704869"
---
# <a name="groupsizedefinition-element"></a>Elemento GroupSizeDefinition

Representa un tamaño de diseño de un grupo de controles en una plantilla personalizada.

## <a name="usage"></a>Uso

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>Tamaño</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Amplíe<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> Medio<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Pequeño<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                 | Descripción                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ColumnBreak**](windowsribbon-element-columnbreak.md)<br/>                     | Puede producirse una o varias veces<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                   | Puede producirse una o varias veces<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**Row**](windowsribbon-element-row.md)<br/>                                     | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                   |
|---------------------------------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse hasta tres veces para cada elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) (una vez por cada *tamaño*).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra una plantilla personalizada básica que incluye los tres tamaños de diseño de grupo que se deben definir con el elemento **GroupSizeDefinition** al crear una plantilla personalizada.


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





