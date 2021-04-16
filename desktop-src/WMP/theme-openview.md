---
title: THEME. openView
description: El método openView abre una vista en una nueva ventana.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEME. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680247"
---
# <a name="themeopenview"></a>THEME. openView

El método **openView** abre una **vista** en una nueva ventana.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Visores*
</dt> <dd>

**Cadena** que especifica el **identificador** de la **vista** que se va a abrir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="examples"></a>Ejemplos


```JScript
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

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





