---
title: Propiedad ScalingPolicy. IdealSizes
description: Representa un contenedor de especificaciones de escala para la plantilla de SizeDefinition preferida, en función del tamaño de la cinta de opciones.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy. IdealSizes (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705167"
---
# <a name="scalingpolicyidealsizes-property"></a>Propiedad ScalingPolicy. IdealSizes

Representa un contenedor de especificaciones de escala para la plantilla de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferida, en función del tamaño de la cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                 | Descripción                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Escala**](windowsribbon-element-scale.md)<br/> | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).

Si se define **ScalingPolicy. IdealSizes** , debe haber una entrada de [**escala**](windowsribbon-element-scale.md) para cada elemento de [**Grupo**](windowsribbon-element-group.md) de un elemento de [**ficha**](windowsribbon-element-tab.md) .

**ScalingPolicy. IdealSizes** son los diseños de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferidos para un [**Grupo**](windowsribbon-element-group.md) de controles.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un [**Grupo**](windowsribbon-element-group.md) mediante la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de la cinta.

El manifiesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de [**escala**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.


```C++
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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





