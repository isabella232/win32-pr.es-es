---
title: Elemento FlowMenuLayout
description: Representa un diseño horizontal con saltos de línea para los elementos de una galería.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Elemento FlowMenuLayout de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442886"
---
# <a name="flowmenulayout-element"></a>Elemento FlowMenuLayout

Representa un diseño horizontal con saltos de línea para los elementos de una galería.

## <a name="usage"></a>Uso

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
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
<td><strong>Columnas</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Especifica el número de elementos que se mostrarán en una sola fila.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Cualquier entero positivo o negativo. <br/> El valor predeterminado es <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Pinza</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Un identificador de tamaño asociado a la lista desplegable de la galería. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Ninguno)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Vertical)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Esquina)<br/> </dt> <dd> Predeterminada. <br/> </dd> </dl></td>
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

El [**elemento VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o **FlowMenuLayout** deben producirse una vez para cada [**elemento DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)

Los elementos se organizan según las propiedades de salto de línea inherentes a los *atributos de* fila *y* columna. Cuando el contenido supera la longitud de una sola línea, el menú interrumpe las líneas, ajusta las líneas y alinea el contenido correctamente.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).

En esta sección de código se muestra la declaración de control [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) con una **especificación FlowMenuLayout.**


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

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** Sí


 

 





