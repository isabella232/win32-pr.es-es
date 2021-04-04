---
title: Elemento VerticalMenuLayout
description: Representa un diseño vertical para los elementos de una galería.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout cinta de opciones de Windows
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "103789406"
---
# <a name="verticalmenulayout-element"></a>Elemento VerticalMenuLayout

Representa un diseño vertical para los elementos de una galería.

## <a name="usage"></a>Uso

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
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
<td><strong>Agarrador</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Un controlador de cambio de tamaño adjunto al menú desplegable de la galería. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Ninguna<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Vertical<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 y versiones más recientes</strong><br/> Resalta todos los elementos de la lista hasta el elemento mouseover actual (en lugar del elemento mouseover, y lo incluye). Se suele usar para varias funciones de <strong>Deshacer</strong> y <strong>rehacer</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Filas</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número de filas de elementos que se van a ver sin desplazamiento. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: integer)<br/> </dt> <dd> Cualquier entero positivo o negativo. <br/> El valor predeterminado es <strong>-1</strong> , que especifica que se muestren tantas filas de elementos como sea posible.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

El elemento **VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) debe aparecer una vez por cada elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico de un elemento **VerticalMenuLayout** .

En esta sección de código se muestran las declaraciones de control de [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .


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
| Puede estar vacío                        | Sí       |



 

 





