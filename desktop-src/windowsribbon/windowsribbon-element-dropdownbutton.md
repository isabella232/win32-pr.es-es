---
title: Elemento DropDownButton
description: Representa un control button Drop-Down estándar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Elemento DropDownButton Windows Cinta de opciones
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08353f4d6c743d92eff08f83e90babb9cc9d075f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623931"
---
# <a name="dropdownbutton-element"></a>Elemento DropDownButton

Representa un control [de botón desplegable](windowsribbon-controls-dropdownbutton.md) estándar.

## <a name="usage"></a>Uso

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.<br/> <br/>
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



| Elemento                                                                             | Descripción                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| **DropDownButton**<br/>                                                       | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                     | Debe producirse al menos una vez<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional o obligatorio, en función del elemento primario.

Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md) [**o SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

**DropDownButton admite** [los modos de](ribbon-applicationmodes.md) aplicación cuando se hospeda en la columna izquierda del menú aplicación.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) y [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) no son elementos secundarios válidos de **DropDownButton** cuando **DropDownButton** es un descendiente de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para **DropDownButton**.

En esta sección de código se muestran las [](windowsribbon-element-group.md) declaraciones del comando **DropDownButton,** con un grupo asociado que funciona como contenedor primario para el **elemento DropDownButton.**


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



En esta sección de código se muestran las declaraciones de control **DropDownButton.**


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control De botón desplegable](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

