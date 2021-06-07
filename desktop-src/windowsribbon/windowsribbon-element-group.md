---
title: Group, elemento
description: Representa un control Group que funciona como contenedor para un grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Agrupación de elementos de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442876"
---
# <a name="group-element"></a>Group, elemento

Representa un control [Group](windowsribbon-controls-group.md) que funciona como contenedor para un grupo de elementos.

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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena que contiene una lista separada por comas de enteros entre 0 y 31.<br/> El espacio en blanco es válido y se omite.<br/> Longitud máxima: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cuando se especifica, el valor de <em>SizeDefinition</em> se restringe a una de las plantillas <a href="windowsribbon-templates.md">de diseño</a> definidas por el marco de la cinta de opciones. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cualquier secuencia de cero o más caracteres.<br/> La longitud máxima es sin enlazar.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                             | Descripción                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Puede producirse una o varias veces<br/> <br/> |
| [**Casilla**](windowsribbon-element-checkbox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Puede producirse una o varias veces<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Puede producirse como máximo una vez<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Puede producirse una o varias veces<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Puede producirse como máximo una vez<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Puede producirse una o varias veces<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Puede producirse una o varias veces<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                             |
|-----------------------------------------------------|
| [**pestaña**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para cada [**elemento Tab.**](windowsribbon-element-tab.md)

[**Tab admite**](windowsribbon-element-tab.md) los [modos de aplicación](ribbon-applicationmodes.md).

El marcado de la cinta de opciones solo es válido cuando los elementos secundarios de **Group** corresponden a la plantilla especificada para *SizeDefinition.*

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el uso de una plantilla personalizada en un **grupo**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> <dt>

[Control de grupo](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

