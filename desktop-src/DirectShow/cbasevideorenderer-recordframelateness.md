---
description: El método RecordFrameLateness registra la hora a la que se produjo la representación y recopila estadísticas de la página de propiedades.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Método CBaseVideoRenderer.RecordFrameLateness (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89682799ce71df8a8b08feb01454db3ec4fdd475a4107fcdb96e3a215a416657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814105"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>Método CBaseVideoRenderer.RecordFrameLateness

El `RecordFrameLateness` método registra la hora a la que se produjo la representación y recopila estadísticas de la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*trLate* 
</dt> <dd>

Valor que indica el retraso de la muestra más allá de su tiempo debido, en unidades de tiempo de referencia.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tiempo de interframe, en unidades de tiempo de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




