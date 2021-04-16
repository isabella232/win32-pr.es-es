---
title: TEXT. wordWrap
description: El atributo wordWrap especifica o recupera un valor que indica si el ajuste de palabras está habilitado o deshabilitado.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- TEXT. wordWrap Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650088"
---
# <a name="textwordwrap"></a>TEXT. wordWrap

El atributo **WordWrap** especifica o recupera un valor que indica si el ajuste de palabras está habilitado o deshabilitado.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | El ajuste de palabra está habilitado.                                                                             |
| false | Predeterminada. El ajuste de palabra está deshabilitado. Si el texto no cabe en el control, el texto se recorta. |



 

## <a name="remarks"></a>Observaciones

El control de texto no separa palabras. Si una palabra se extiende más allá del ancho del control, se emplea el ajuste automático de línea para colocar la palabra en la línea siguiente. Si una sola palabra es más larga que el ancho del control, esa palabra se recorta y ocupa una sola línea.

Si no se especifica el atributo **width** , se omite **WordWrap** y se cambia el tamaño del control de texto en lugar de ajustar el texto.

Si se desean saltos de línea en ubicaciones concretas, se deben especificar explícitamente en el **valor** mediante "&\# 13;" o " \\ r". Si se usa el último formulario al especificar el valor directamente, la cadena debe ir precedida de "JScript:" y el valor real debe estar rodeado por comillas simples, como se muestra a continuación. Esto no es necesario si el valor se establece dinámicamente desde un controlador de eventos.

Si **WordWrap** está establecido en true y no se especifica la **información sobre herramientas** , la información sobre herramientas mostrará el texto completo del atributo **Value** . Si no se desea información sobre herramientas, establezca la **información sobre herramientas** en "" (cadena vacía).

## <a name="examples"></a>Ejemplos


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AmbientAttributes. width**](ambientattributes-width.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXTO. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





