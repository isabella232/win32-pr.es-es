---
title: Elemento VerticalMenuLayout
description: Representa un diseño vertical para los elementos de una galería.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444056"
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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Pinza</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Un identificador de tamaño asociado a la lista desplegable de la galería. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Ninguno)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Vertical)<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 y versiones más recientes</strong><br/> Resalta todos los elementos de la lista hasta el elemento actual del mouseover (en lugar de solo el elemento de mouseover). Normalmente se usa para varias <strong>funcionalidades deshacer</strong> <strong>y rehacer.</strong><br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Filas</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número de filas de elementos que se verán sin desplazarse. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Cualquier entero positivo o negativo. <br/> El valor predeterminado <strong>es -1,</strong> que especifica que se muestren tantas filas de elementos como sea posible.<br/> </dd> </dl></td>
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



## <a name="remarks"></a>Comentarios

Necesario.

El **elemento VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deben producirse una vez para cada [**elemento DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para un **elemento VerticalMenuLayout.**

En esta sección de código se muestran las declaraciones de control [**InRibbonGallery.**](windowsribbon-element-inribbongallery.md)


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


- **Sistema mínimo admitido:** Windows 7 
- **Puede estar vacío:** Sí



 

 





