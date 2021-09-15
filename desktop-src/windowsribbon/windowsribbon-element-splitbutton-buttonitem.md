---
title: SplitButton.ButtonItem, propiedad
description: Representa un contenedor para un botón o botón de alternancia que expone el comando predeterminado de un botón de división.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Propiedad SplitButton.ButtonItem Windows cinta de opciones
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359967"
---
# <a name="splitbuttonbuttonitem-property"></a>SplitButton.ButtonItem, propiedad

Representa un contenedor para un [botón o](windowsribbon-controls-button.md) [botón de](windowsribbon-controls-togglebutton.md) alternancia que expone el comando predeterminado de un botón [de división](windowsribbon-controls-splitbutton.md).

## <a name="usage"></a>Uso

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Descripción                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>             | Puede producirse como máximo una vez<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para [**cada SplitButton**](windowsribbon-element-splitbutton.md).

Cada **SplitButton.ButtonItem** solo puede contener un [**elemento**](windowsribbon-element-button.md) secundario [**Button o ToggleButton.**](windowsribbon-element-togglebutton.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el [botón De división](windowsribbon-controls-splitbutton.md).

En esta sección de código se muestran las declaraciones [**SplitButton**](windowsribbon-element-splitbutton.md) y **SplitButton.ButtonItem** Command, con un grupo asociado que funciona como contenedor primario para el **elemento SplitButton.** [](windowsribbon-element-group.md)


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



En esta sección de código se muestran las [**declaraciones**](windowsribbon-element-splitbutton.md) de control **SplitButton y SplitButton.ButtonItem.**


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

 

 





