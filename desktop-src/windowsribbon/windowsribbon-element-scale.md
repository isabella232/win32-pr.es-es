---
title: Elemento Scale
description: Representa el tamaño y la preferencia de diseño de un grupo de controles a través de un par de grupo, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Cinta de opciones de ventanas de elementos de escala
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420198"
---
# <a name="scale-element"></a>Elemento Scale

Representa el tamaño y la preferencia de diseño de un [**Grupo**](windowsribbon-element-group.md) de controles a través de un par {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Uso

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
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
<td><strong>Grupo</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>Sí<br/></td>
<td>Debe corresponder a un <a href="windowsribbon-element-group.md"><strong>Grupo</strong></a> <em>CommandName</em>existente.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena o un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tamaño</strong><br/></td>
<td>xs:string<br/></td>
<td>Sí<br/></td>
<td>Este valor debe corresponder a uno de los tamaños válidos para el atributo <em>SizeDefinition</em> del <a href="windowsribbon-element-group.md"><strong>Grupo</strong></a> de controles asociado especificado en <em>Group</em>. <br/> Restringido a uno de los siguientes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> Emergente<br/> </dt> <dd> Diseño de control idéntico al que se <code>Large</code> hospeda en un panel desplegable o un elemento emergente.<br/> </dd> <dt><span></span><span></span><strong></strong> Pequeño<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeña.<br/> </dd> <dt><span></span><span></span><strong></strong> Medio<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> mediana.<br/> </dd> <dt><span></span><span></span><strong></strong> Amplíe<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) o [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).

Cada par de atributo (*Grupo*, *tamaño*) debe ser único.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un [**Grupo**](windowsribbon-element-group.md) mediante la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de la cinta.

El manifiesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de **escala** se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
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

 

 





