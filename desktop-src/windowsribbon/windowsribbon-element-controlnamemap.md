---
title: Elemento ControlNameMap
description: Representa un contenedor para los nombres de control en una plantilla de diseño SizeDefinition personalizada.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- ControlNameMap, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42654af7f81730d01f9c699de7041ba24be185e9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442916"
---
# <a name="controlnamemap-element"></a>Elemento ControlNameMap

Representa un contenedor para los nombres de control en una [**plantilla de diseño SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada.

## <a name="usage"></a>Uso

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                 | Descripción                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ControlNameDefinition**](windowsribbon-element-controlnamedefinition.md)<br/> | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                   |
|---------------------------------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento SizeDefinition.**](windowsribbon-element-sizedefinition.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado básico para una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con un **elemento ControlNameMap.**


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

 

 





