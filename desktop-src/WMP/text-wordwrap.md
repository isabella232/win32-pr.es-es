---
title: TEXT.wordWrap
description: El atributo wordWrap especifica o recupera un valor que indica si el ajuste de línea está habilitado o deshabilitado.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Text.wordWrap Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264751"
---
# <a name="textwordwrap"></a>TEXT.wordWrap

El **atributo wordWrap** especifica o recupera un valor que indica si el ajuste de línea está habilitado o deshabilitado.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | El ajuste de palabra está habilitado.                                                                             |
| false | Predeterminada. El ajuste de palabra está deshabilitado. Si el texto no cabe dentro del control , el texto se recorta. |



 

## <a name="remarks"></a>Observaciones

El control Texto no divide las palabras. Si una palabra se extiende más allá del ancho del control, se emplea el ajuste de línea para mover la palabra a la línea siguiente. Si una sola palabra es mayor que el ancho del control, esa palabra se recorta y ocupa una sola línea.

Si no **se especifica** el atributo width, **wordWrap** se omite y el control Text cambia de tamaño en lugar de ajustar el texto.

Si se desean saltos de línea en ubicaciones concretas, se deben especificar explícitamente en **value** mediante "&\# 13;" o \\ "r". Si se usa la última forma al especificar el valor directamente, la cadena debe tener el prefijo "JScript:" y el valor real debe ir entre comillas simples, como se muestra a continuación. Esto no es necesario si el valor se establece dinámicamente desde dentro de un controlador de eventos.

Si **wordWrap** se establece en true y no se especifica **toolTip,** la información sobre herramientas mostrará el texto completo del **atributo value.** Si no se desea ninguna información sobre herramientas, establezca **toolTip** en "" (cadena vacía).

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AmbientAttributes.width**](ambientattributes-width.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> </dl>

 

 





