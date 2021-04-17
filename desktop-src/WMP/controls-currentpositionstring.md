---
title: Controls. currentPositionString
description: La propiedad currentPositionString recupera la posición actual en el elemento multimedia como una cadena con el formato HH MM SS (horas, minutos y segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Media Player de Windows Controls. currentPositionString
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
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700129"
---
# <a name="controlscurrentpositionstring"></a>Controls. currentPositionString

La propiedad **currentPositionString** recupera la posición actual en el elemento multimedia como una **cadena** con el formato HH: mm: SS (horas, minutos y segundos).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Si el elemento multimedia tiene menos de una hora, la parte HH: no se incluye.

> [!Note]  
> Debe incluir código para detener el temporizador cuando el elemento multimedia está detenido o en pausa.

 

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se inicia un temporizador HTML que muestra la posición actual del archivo multimedia en intervalos de un segundo. Se creó un elemento de texto HTML denominado mi texto para mostrar la posición actual. El objeto **Player** se creó con ID = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 





