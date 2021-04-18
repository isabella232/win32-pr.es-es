---
title: THEME. openViewRelative
description: El método openViewRelative abre una vista en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Media Player de Windows de THEME. openViewRelative
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680246"
---
# <a name="themeopenviewrelative"></a>THEME. openViewRelative

El método **openViewRelative** abre una **vista** en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Visores*
</dt> <dd>

**Cadena** que especifica el **identificador** de la **vista** que se va a abrir.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*salido*
</dt> <dd>

**Número** (**Long**) que especifica la distancia inicial en píxeles del borde izquierdo de la **vista** desde el borde izquierdo de la máscara. Un valor negativo indica una posición inicial a la izquierda del borde de la máscara.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Arriba*
</dt> <dd>

**Número** (**Long**) que especifica la posición inicial del borde superior de la **vista** con respecto al borde superior de la máscara. Un valor negativo indica una posición inicial sobre el borde de la máscara.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La posición especificada para la **vista** se usa la primera vez que se llama a este método, después de lo cual el usuario puede arrastrar la **vista** a otra ubicación. La nueva posición se guarda y, en las llamadas posteriores, se usa la posición más reciente.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





