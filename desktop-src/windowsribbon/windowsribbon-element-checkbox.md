---
title: CheckBox, elemento
description: Representa un control de casilla.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox (elemento) cinta de Windows
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104149066"
---
# <a name="checkbox-element"></a>CheckBox, elemento

Representa un control de [casilla](windowsribbon-controls-checkbox.md) .

## <a name="usage"></a>Uso

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>ApplicationDefaults. IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Este atributo solo es válido cuando el elemento <strong>CheckBox</strong> es un elemento secundario de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>. <br/> Restringido a uno de los siguientes valores:<br/>
<blockquote>
[!Note]<br />
La <strong>casilla</strong> no admite un estado terciario o indeterminado.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                                                                   |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Observaciones

Opcional o obligatorio, dependiendo del elemento primario.

Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el elemento **CheckBox** .

En esta sección de código se muestran las declaraciones del comando **CheckBox** .


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



En esta sección de código se muestran las declaraciones del control **CheckBox** .


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Check Box (control)](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





