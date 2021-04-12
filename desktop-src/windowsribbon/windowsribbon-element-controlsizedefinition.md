---
title: Elemento ControlSizeDefinition
description: Representa el estilo de diseño de un grupo de controles en una plantilla personalizada.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- ControlSizeDefinition cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358147"
---
# <a name="controlsizedefinition-element"></a>Elemento ControlSizeDefinition

Representa el estilo de diseño de un grupo de controles en una plantilla personalizada.

## <a name="usage"></a>Uso

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
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
<td><strong>Nombrecontrol</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ImageSize</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Amplíe<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Pequeño<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsImageVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsLabelVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsPopup</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                             |
|-------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Row**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md)o [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado básico de una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con varios elementos **ControlSizeDefinition** .


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
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





