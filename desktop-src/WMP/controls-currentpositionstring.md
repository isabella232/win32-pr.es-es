---
title: Controls.currentPositionString
description: La propiedad currentPositionString recupera la posición actual en el elemento multimedia como una cadena con formato HH MM SS (horas, minutos y segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls.currentPositionString Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640f0f97e3fa4c4054df17ea92304ad7721c770d9cb9b56436dcf810b9c083ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651995"
---
# <a name="controlscurrentpositionstring"></a>Controls.currentPositionString

La **propiedad currentPositionString** recupera la posición actual  en el elemento multimedia como una cadena con formato HH:MM:SS (horas, minutos y segundos).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Comentarios

Si el elemento multimedia tiene menos de una hora de duración, no se incluye la parte HH:.

> [!Note]  
> Debe incluir código para detener el temporizador cuando el elemento multimedia está detenido o en pausa.

 

## <a name="examples"></a>Ejemplos

En el JScript siguiente se inicia un temporizador HTML que muestra la posición actual del archivo multimedia en intervalos de un segundo. Se creó un elemento HTML TEXT denominado MyText para mostrar la posición actual. El **objeto Player** se creó con id. = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





