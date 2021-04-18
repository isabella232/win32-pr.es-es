---
title: THEME. closeView
description: El método closeView cierra una vista abierta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Media Player de Windows de THEME. closeView
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649738"
---
# <a name="themecloseview"></a>THEME. closeView

El método **closeView** cierra una **vista** abierta.

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*Vista*
</dt> <dd>

**Cadena** que especifica el **identificador** de la **vista** que se va a cerrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="examples"></a>Ejemplos


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





