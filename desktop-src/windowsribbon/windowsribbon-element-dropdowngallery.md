---
title: Elemento DropDownGallery
description: Representa un control de galería de Drop-Down con un menú basado en la galería.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533226"
---
# <a name="dropdowngallery-element"></a>Elemento DropDownGallery

Representa un control de [Galería desplegable](windowsribbon-controls-dropdowngallery.md) con un menú basado en la galería.

## <a name="usage"></a>Uso

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.<br/> El espacio en blanco es válido y se omite.<br/> Longitud máxima: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería. <br/>
<blockquote>
[!Note]<br />
Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Command</code> .
</blockquote>
<br/> Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> El valor predeterminado es -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> El valor predeterminado es -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Descendente<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> U<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Salido<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Superpone<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Correcta<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Primeras<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Elementos<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Comandos<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                           | Descripción                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botón**](windowsribbon-element-button.md)<br/>                                         | Puede producirse una o varias veces<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                                     | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | Debe aparecer exactamente una vez<br/> <br/>     |
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | Puede aparecer como máximo una vez<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>
<td>Cuando está contenido en un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>. Este elemento solo se admite en el primer nivel y no debe tener elementos secundarios.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**splitButton**](windowsribbon-element-splitbutton.md) .

**DropDownGallery** admite los [modos de aplicación](ribbon-applicationmodes.md).

En la captura de pantalla siguiente se muestra el control [Galería desplegable](windowsribbon-controls-dropdowngallery.md) de la cinta de opciones de Microsoft Paint para Windows 7.

![captura de pantalla de un control de Galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para **DropDownGallery**.

En esta sección de código se muestran las declaraciones de comandos de **DropDownGallery** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **DropDownGallery** .


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



En esta sección de código se muestran las declaraciones de control de **DropDownGallery** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Control Galería desplegable**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Ejemplo de la galería](windowsribbon-gallerysample.md)
</dt> </dl>

 

