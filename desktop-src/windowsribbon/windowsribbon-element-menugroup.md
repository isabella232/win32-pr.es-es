---
title: Elemento MenuGroup
description: Representa un contenedor de controles que se mostrarán en una galería, un menú o una barra de herramientas.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Elemento MenuGroup Windows cinta de opciones
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dad52aebe4a90d132827f01400fc7a1f2bbf1fde
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624721"
---
# <a name="menugroup-element"></a>Elemento MenuGroup

Representa un contenedor de controles que se mostrarán en una galería, un menú o una barra de herramientas.

## <a name="usage"></a>Uso

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>Clase</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Especifica el tamaño y el estilo de diseño de los elementos de la interfaz de usuario del menú.<br/> Un recurso de imagen se puede proporcionar en dos tamaños (grande y pequeño) y asociarse con el elemento en el marcado mediante los elementos de propiedad <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> y <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages.</strong></a> Si solo se proporciona una imagen, el marco cambia su tamaño según sea necesario.<br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems)<br/> </dt> <dd> Predeterminada. <br/> Estilo: imagen pequeña y texto sin resaltar.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems)<br/> </dt> <dd> Estilo: imagen grande y texto en negrita.<br/>
<blockquote>
[!Note]<br />
Si <strong>MenuGroup</strong> es un elemento secundario de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, el <em>atributo Class</em> se omite y el marco aplica un estilo de <code>MajorItems</code> .
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                             | Descripción                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Puede producirse como máximo una vez<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse al menos una vez para cada [**elemento ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups,**](windowsribbon-element-splitbutton-menugroups.md) [**MiniToolbar**](windowsribbon-element-minitoolbar.md)o [**SplitButtonGallery.MenuGroups.**](windowsribbon-element-splitbuttongallery-menugroups.md)

Si [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario, **MenuGroup** se restringe a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).

Si [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)o [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) es el elemento primario, **MenuGroup** se restringe a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**CheckBox,**](windowsribbon-element-checkbox.md) **DropDownButton,** [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton.**](windowsribbon-element-togglebutton.md)

Si [**MiniToolbar**](windowsribbon-element-minitoolbar.md) es el elemento primario, **MenuGroup** se restringe a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).

El atributo Class no es necesario cuando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario. El marco aplica un valor de MajorItems para el atributo Class.

Cuando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario, el atributo Class no es necesario.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**SplitButton**](windowsribbon-element-splitbutton.md) con un **elemento MenuGroup.**

En esta sección de código se muestran las [**declaraciones de**](windowsribbon-element-splitbutton.md) los comandos SplitButton y **MenuGroup** con un recurso de imagen grande y pequeño. También se [**declara**](windowsribbon-element-group.md) un grupo asociado que actúa como contenedor primario para el elemento **SplitButton.**


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



En esta sección de código se muestran [**las declaraciones de**](windowsribbon-element-splitbutton.md) control SplitButton y **MenuGroup** con `StandardItems` y `MajorItems` .


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



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)
</dt> <dt>

[Grupo de menús](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





