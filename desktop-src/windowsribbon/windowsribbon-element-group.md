---
title: Group, elemento
description: Representa un control de grupo que funciona como un contenedor para un grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Cinta de opciones de Windows elemento de grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421039"
---
# <a name="group-element"></a>Group, elemento

Representa un control de [Grupo](windowsribbon-controls-group.md) que funciona como un contenedor para un grupo de elementos.

## <a name="usage"></a>Uso

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.<br/> El espacio en blanco es válido y se omite.<br/> Longitud máxima: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cuando se especifica, el valor de <em>SizeDefinition</em> está restringido a una de las <a href="windowsribbon-templates.md">plantillas de diseño</a> definidas por el marco de la cinta de opciones. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cualquier secuencia de cero o más caracteres.<br/> La longitud máxima es sin límite.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                             | Descripción                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botón**](windowsribbon-element-button.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Puede aparecer como máximo una vez<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Puede aparecer como máximo una vez<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                             |
|-----------------------------------------------------|
| [**Tabulación**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada elemento de [**ficha**](windowsribbon-element-tab.md) .

La [**pestaña**](windowsribbon-element-tab.md) admite los [modos de aplicación](ribbon-applicationmodes.md).

El marcado de la cinta de opciones solo es válido cuando los elementos secundarios del **Grupo** corresponden a la plantilla especificada para *SizeDefinition*.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el uso de una plantilla personalizada en un **Grupo**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> <dt>

[Control de grupo](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

