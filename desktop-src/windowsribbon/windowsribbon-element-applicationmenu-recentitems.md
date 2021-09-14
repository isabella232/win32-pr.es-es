---
title: Propiedad ApplicationMenu.RecentItems
description: Representa un contenedor para el control Elementos recientes en el menú Aplicación.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- ApplicationMenu.RecentItems, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360614"
---
# <a name="applicationmenurecentitems-property"></a>Propiedad ApplicationMenu.RecentItems

Representa un contenedor para el control [Elementos recientes](windowsribbon-controls-recentitems.md) en el menú de [la aplicación](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
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
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Descripción                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**RecentItems**](windowsribbon-element-recentitems.md)<br/> | Debe producirse exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**elemento ApplicationMenu.**](windowsribbon-element-applicationmenu.md)

El [control Elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación de cinta de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el control [Elementos recientes.](windowsribbon-controls-recentitems.md)

En el ejemplo siguiente se muestra [**una declaración De comando RecentItems.**](windowsribbon-element-recentitems.md)


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



En el ejemplo siguiente se muestra la **declaración de controles ApplicationMenu.RecentItems** y [**RecentItems**](windowsribbon-element-recentitems.md) asociada.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control Menú de la aplicación](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Control Elementos recientes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





