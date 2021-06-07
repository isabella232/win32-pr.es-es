---
title: Elemento SplitButton
description: Representa un control Split Button estándar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Elemento SplitButton de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf03d85dd0402548d02f107dafb209b68c13bb72
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444406"
---
# <a name="splitbutton-element"></a>Elemento SplitButton

Representa un control [Split Button](windowsribbon-controls-splitbutton.md) estándar.

## <a name="usage"></a>Uso

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Solo es válido <a href="windowsribbon-element-menugroup.md"><strong>si MenuGroup</strong></a> es el elemento primario.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena que contiene una lista separada por comas de enteros entre 0 y 31.<br/> El espacio en blanco es válido y se omite.<br/> Longitud máxima: 250 caracteres. <br/> </dd> </dl></td>
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



| Elemento                                                                                   | Descripción                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                 | Puede producirse una o varias veces<br/> <br/> |
| [**Casilla**](windowsribbon-element-checkbox.md)<br/>                             | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |
| **SplitButton**<br/>                                                                | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Puede producirse como máximo una vez<br/> <br/>      |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Puede producirse como máximo una vez<br/> <br/>      |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

**SplitButton** admite [modos de](ribbon-applicationmodes.md) aplicación cuando se hospeda en la columna izquierda del menú de la aplicación.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) y [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) no son elementos secundarios válidos de [**DropDownButton**](windowsribbon-element-dropdownbutton.md) cuando **DropDownButton** es un descendiente de [**ApplicationMenu.**](windowsribbon-element-applicationmenu.md)

[**SplitButton.MenuGroups debe**](windowsribbon-element-splitbutton-menugroups.md) producirse una vez si lo siguiente no está presente como elementos secundarios de **SplitButton**:

-   [**Button**](windowsribbon-element-button.md)
-   [**Casilla**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
-   [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Estos controles se tratan como elementos secundarios de un único [**elemento SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) predeterminado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el [botón Dividir](windowsribbon-controls-splitbutton.md).

En esta sección de código se muestran las declaraciones del comando **SplitButton,** con un [**grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario para el **elemento SplitButton.**


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



En esta sección de código se muestran las declaraciones de control **SplitButton.**


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

- **Sistema mínimo admitido:** Windows 7 
- **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Split Button (Control)](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

