---
title: Elemento InRibbonGallery
description: Representa la galería de In-Ribbon, un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones. Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery cinta de opciones de Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "104077479"
---
# <a name="inribbongallery-element"></a>Elemento InRibbonGallery

Representa la [Galería en cinta](windowsribbon-controls-inribbongallery.md), un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones. Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.

## <a name="usage"></a>Uso

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
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
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Junto con <em>ItemWidth</em>, determina el tamaño de la imagen del elemento que se muestra en el control de la galería. <br/>
<blockquote>
[!Note]<br />
Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> El valor predeterminado es -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Junto con <em>ItemHeight</em>, determina el tamaño de la imagen del elemento que se muestra en el control de la galería. <br/>
<blockquote>
[!Note]<br />
Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> El valor predeterminado es -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número máximo de columnas que muestra el <strong>InRibbonGallery</strong> , por ejemplo, en la lista desplegable de diseño de grupo <em>grande</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número máximo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño del grupo <em>mediano</em> , antes de cambiar a un diseño <em>grande</em> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número máximo de filas para el diseño de los elementos <strong>InRibbonGallery</strong> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> El valor predeterminado es 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número mínimo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño de grupo <em>grande</em> , antes de cambiar a <em>medio</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número mínimo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño del grupo <em>mediano</em> , antes de cambiar a <em>pequeño</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>No<br/></td>
<td>Especifica dónde se muestra la etiqueta del elemento, en relación con la imagen. <br/> Restringido a uno de los siguientes valores:<br/> <br/>
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
| [**Casilla**](windowsribbon-element-checkbox.md)<br/>                                     | Puede producirse una o varias veces<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Debe aparecer exactamente una vez<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Puede aparecer como máximo una vez<br/> <br/>      |
| [**Botón**](windowsribbon-element-button.md)<br/>                                       | Puede producirse una o varias veces<br/> <br/> |
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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Opcional.

Puede aparecer como máximo una vez por cada elemento de [**Grupo**](windowsribbon-element-group.md) o [**ControlGroup**](windowsribbon-element-controlgroup.md) .

En la captura de pantalla siguiente se muestra el control [Galería de cintas en cinta](windowsribbon-controls-inribbongallery.md) de opciones de Microsoft Paint para Windows 7.

![captura de pantalla de un control de la galería de la cinta de opciones en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico de una [Galería de la cinta de](windowsribbon-controls-inribbongallery.md)opciones.

En esta sección de código se muestran las declaraciones de comandos de **InRibbonGallery** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **InRibbonGallery** .


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



En esta sección de código se muestran las declaraciones de control de **InRibbonGallery** .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de la galería de la cinta de opciones](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[Ejemplo de la galería](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





