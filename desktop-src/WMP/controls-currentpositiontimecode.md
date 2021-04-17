---
title: Controls. currentPositionTimecode
description: La propiedad currentPositionTimecode especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Media Player de Windows Controls. currentPositionTimecode
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698653"
---
# <a name="controlscurrentpositiontimecode"></a>Controls. currentPositionTimecode

La propiedad **currentPositionTimecode** especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

El código de tiempo SMPTE proporciona una forma estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción. Si un archivo multimedia digital admite código de tiempo SMPTE, Windows Media Player puede recuperar la información de posición del código de tiempo actual o buscar un fotograma de vídeo identificado por una **cadena** de código de tiempo determinada.

El código de tiempo SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado, el marco designado como tiempo cero. Normalmente, el marco de cero de tiempo es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.

La **cadena** de código de tiempo está en el intervalo de formato \[  \] *HH*:*mm*:*SS*.*FF* donde \[ *Range* \] representa el intervalo, *HH* representa las horas, *mm* representa los minutos, *SS* representa los segundos y *FF* representa los fotogramas. Al especificar un valor mediante **currentPositionTimecode**, debe incluir los ocho dígitos usando ceros como marcadores de posición.

El \[  \] especificador de intervalo se corresponde con el miembro **wRange** de la estructura de datos de la **extensión de código de \_ tiempo \_ \_ WMT** del formato de Windows Media. Para obtener más información acerca de los intervalos de código de tiempo, vea el SDK de Windows Media Format.

Solo se admite la especificación y recuperación de **currentPositionTimecode** para los archivos que contienen información de código de tiempo SMPTE.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se especifica **currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas. El objeto **Player** se creó con ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 





