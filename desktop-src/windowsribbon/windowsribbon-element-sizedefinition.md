---
title: Elemento SizeDefinition
description: Representa una plantilla de diseño personalizada de controles de cinta de opciones.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Cinta de opciones del Windows SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 212cd7267db87b3892daad2868afab1358cec4c1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629916"
---
# <a name="sizedefinition-element"></a>Elemento SizeDefinition

Representa una plantilla de diseño personalizada de controles de cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
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
<td><strong>Nombre</strong><br/></td>
<td>xs:positiveInteger o xs:string o xs:token<br/></td>
<td>Sí<br/></td>
<td>Cuando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> es el elemento primario; de lo contrario, es opcional.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string o xs:token)<br/> </dt> <dd> Una cadena o un valor entero entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                             | Descripción                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**ControlNameMap**](windowsribbon-element-controlnamemap.md)<br/>           | Puede producirse como máximo una vez<br/> <br/>   |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Debe producirse al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                                   |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento Group.**](windowsribbon-element-group.md)

Puede producirse una o varias veces para cada [**elemento Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)

Las plantillas de diseño del marco [de opciones](windowsribbon-templates.md) predefinidas se especifican con el *atributo SizeDefinition* del [**elemento Group.**](windowsribbon-element-group.md)

Si no se [**declara un elemento ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondiente para cada elemento [**Group**](windowsribbon-element-group.md) de un elemento [**Tab,**](windowsribbon-element-tab.md) se producirá un error de validación.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra una plantilla personalizada básica.


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


- **Sistema mínimo admitido:** Windows 7 
- **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





