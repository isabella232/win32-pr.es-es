---
title: SplitButton.MenuGroups, propiedad
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control Split Button estándar.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- SplitButton.MenuGroups, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359966"
---
# <a name="splitbuttonmenugroups-property"></a>SplitButton.MenuGroups, propiedad

Representa un contenedor para un conjunto de elementos de menú desplegable en un control [Split Button](windowsribbon-controls-splitbutton.md) estándar.

## <a name="usage"></a>Uso

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Debe producirse al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para [**cada SplitButton**](windowsribbon-element-splitbutton.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el [botón De división](windowsribbon-controls-splitbutton.md).

En esta sección de código se muestran las declaraciones del comando [](windowsribbon-element-group.md) [**SplitButton**](windowsribbon-element-splitbutton.md) y **SplitButton.MenuGroups,** con un grupo asociado que funciona como contenedor primario para el **elemento SplitButton.**


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



En esta sección de código se muestran las [**declaraciones**](windowsribbon-element-splitbutton.md) de control **SplitButton y SplitButton.MenuGroups.**


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control Botón de división](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





