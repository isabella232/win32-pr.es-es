---
title: Elemento RecentItems
description: Representa el control Elementos recientes en el menú De la aplicación.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Cinta de opciones del Windows RecentItems
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa1354caadc14cf15b34333c81bff1211e1fbc8c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631953"
---
# <a name="recentitems-element"></a>Elemento RecentItems

Representa el [control Elementos recientes](windowsribbon-controls-recentitems.md) en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).

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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>No<br/></td>
<td>Número de elementos recientes que se mostrarán.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)<br/> </dt> <dd> Valor entero de 0 o superior.<br/> El valor predeterminado <strong>es 10.</strong><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse exactamente una vez [**para cada elemento ApplicationMenu.RecentItems.**](windowsribbon-element-applicationmenu-recentitems.md)

El [control Elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación de cinta de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el control [Elementos recientes.](windowsribbon-controls-recentitems.md)

En el ejemplo siguiente se muestra **una declaración De comando RecentItems.**


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



En el ejemplo siguiente se muestra la **declaración de controles RecentItems** asociada.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** Sí


## <a name="see-also"></a>Vea también

<dl> <dt>

[Control Menú de la aplicación](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Control Elementos recientes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





