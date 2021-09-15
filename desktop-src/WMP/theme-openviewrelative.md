---
title: THEME.openViewRelative
description: El método openViewRelative abre una vista en una nueva ventana en una posición inicial especificada con respecto a la esquina superior izquierda de la máscara.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME.openViewRelative Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258727"
---
# <a name="themeopenviewrelative"></a>THEME.openViewRelative

El **método openViewRelative** abre una **vista** en una nueva ventana en una posición inicial especificada con respecto a la esquina superior izquierda de la máscara.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Vista*
</dt> <dd>

Cadena **que** especifica el **identificador de** la **vista** que se abrirá.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*Izquierda*
</dt> <dd>

Número  **(long)** que especifica la distancia inicial en píxeles del borde izquierdo de **LA VISTA** desde el borde izquierdo de la máscara. Un valor negativo indica una posición inicial a la izquierda del borde de la máscara.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Arriba*
</dt> <dd>

Número  (**long**) que especifica la posición inicial del borde superior de **VIEW** con respecto al borde superior de la máscara. Los valores negativos indican una posición inicial encima del borde de la máscara.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La posición especificada para **VIEW** se usa la primera vez que se llama a este método, después de lo cual el usuario puede arrastrar la **vista** a otra ubicación. Se guarda la nueva posición y, en las llamadas posteriores, se usa la posición más reciente.

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
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





