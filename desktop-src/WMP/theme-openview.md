---
title: THEME.openView
description: El método openView abre una vista en una nueva ventana.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEME.openView Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258735"
---
# <a name="themeopenview"></a>THEME.openView

El **método openView** abre **una vista** en una nueva ventana.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Vista*
</dt> <dd>

Cadena **que** especifica el **identificador de** la **vista** que se abre.

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





