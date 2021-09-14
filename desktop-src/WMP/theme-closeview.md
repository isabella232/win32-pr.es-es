---
title: THEME.closeView
description: El método closeView cierra una vista abierta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME.closeView Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073198"
---
# <a name="themecloseview"></a>THEME.closeView

El **método closeView** cierra una vista **abierta.**

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

Cadena **que** especifica el **identificador de** **VIEW** que se cerrará.

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





