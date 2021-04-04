---
title: Elemento RecentItems
description: Representa el control de elementos recientes en el menú de la aplicación.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems cinta de opciones de Windows
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104077259"
---
# <a name="recentitems-element"></a>Elemento RecentItems

Representa el control de [elementos recientes](windowsribbon-controls-recentitems.md) en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
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
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>No<br/></td>
<td>Número de elementos recientes que se van a mostrar.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: nonNegativeInteger)<br/> </dt> <dd> Valor entero de 0 o superior.<br/> El valor predeterminado es <strong>10</strong>.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez para cada elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

El control [elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación de cinta.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el control de [elementos recientes](windowsribbon-controls-recentitems.md) .

En el ejemplo siguiente se muestra una declaración de comando **RecentItems** .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



En el ejemplo siguiente se muestra la declaración de controles **RecentItems** asociados.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de menú de la aplicación](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Control de elementos recientes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





