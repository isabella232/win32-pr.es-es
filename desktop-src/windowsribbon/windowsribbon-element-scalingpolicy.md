---
title: Elemento ScalingPolicy
description: Representa un contenedor para las especificaciones de escalado.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Cinta de opciones de Windows del elemento ScalingPolicy
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444996"
---
# <a name="scalingpolicy-element"></a>Elemento ScalingPolicy

Representa un contenedor para las especificaciones de escalado.

## <a name="usage"></a>Uso

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                       | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Escala**](windowsribbon-element-scale.md)<br/>                                       | Puede producirse una o varias veces<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Puede producirse como máximo una vez<br/> <br/>      |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse una vez para [**cada Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).

El **elemento ScalingPolicy** contiene un manifiesto de declaraciones [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) y [**Scale**](windowsribbon-element-scale.md) que especifican preferencias de diseño adaptable para uno o varios elementos [**Group**](windowsribbon-element-group.md) cuando se cambia el tamaño de la cinta.

La lista de [**declaraciones de**](windowsribbon-element-scale.md) escala debe estar en orden descendente de tamaños válidos (grande, mediano, pequeño, emergente) para el [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) asociado al [**elemento Group.**](windowsribbon-element-group.md)

> [!Note]  
> Se recomienda encarecidamente que se especifiquen los detalles adecuados de la directiva de escalado para que una cinta de opciones pueda representarse sin barras de desplazamiento al cambiar el tamaño a un ancho de 300 píxeles a 96 puntos por pulgada (ppp).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un grupo [**a**](windowsribbon-element-group.md) través de la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition de**](windowsribbon-element-sizedefinition.md) la cinta de opciones.

El **manifiesto ScalingPolicy** de este ejemplo especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, los [**elementos Scale**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de conserción, en orden descendente de tamaño, de cada grupo.


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

- **Sistema mínimo admitido:** Windows 7 
- **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





