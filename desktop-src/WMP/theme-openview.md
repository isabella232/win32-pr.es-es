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
ms.openlocfilehash: 5e5dd33760cb86ef1f85f7efd8a3ff38cb36f0408076555e2fe8732ffb53779a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466615"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





