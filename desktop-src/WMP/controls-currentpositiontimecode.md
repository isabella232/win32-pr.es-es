---
title: Controls.currentPositionTimecode
description: La propiedad currentPositionTimecode especifica o recupera la posición actual en el elemento multimedia actual con un formato de código de hora. Esta propiedad admite actualmente código de hora SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls.currentPositionTimecode Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967704"
---
# <a name="controlscurrentpositiontimecode"></a>Controls.currentPositionTimecode

La **propiedad currentPositionTimecode** especifica o recupera la posición actual en el elemento multimedia actual con un formato de código de hora. Esta propiedad admite actualmente código de hora SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Observaciones

El código de tiempo SMPTE proporciona una manera estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción. Si un archivo multimedia digital admite código de tiempo SMPTE, Reproductor de Windows Media recuperar la información de posición del código de hora actual o buscar en un fotograma de vídeo identificado por una cadena de código de hora **determinada.**

El código de tiempo de SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado que el fotograma designa como tiempo cero. Normalmente, el período de tiempo cero es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.

El código de **hora Cadena** está en el intervalo \[ *de formato* \] *hh*:*mm*:*ss*.*ff,* \[ *donde range* \] representa el intervalo, *hh* representa horas, *mm* representa minutos, *ss* representa segundos y *ff* representa fotogramas. Al especificar un valor mediante **currentPositionTimecode**, debe incluir los ocho dígitos usando ceros como marcadores de posición.

El especificador de intervalo corresponde al miembro wRange de la estructura Windows formato multimedia \[  \] **WMT \_ TIMECODE \_ EXTENSION \_ DATA.**  Para obtener más información sobre los intervalos de código de tiempo, consulte el SDK Windows Media Format.

La especificación y recuperación **de currentPositionTimecode** solo se admite para los archivos que contienen información de código de tiempo de SMPTE.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **especifica currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas. El **objeto Player** se creó con id. = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 





