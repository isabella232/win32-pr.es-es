---
description: El método RecordFrameLateness registra el tiempo que se produce la representación y recopila las estadísticas de la página de propiedades.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Método CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
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
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679101"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>CBaseVideoRenderer. RecordFrameLateness, método

El `RecordFrameLateness` método registra el tiempo que se produce la representación y recopila estadísticas de la página de propiedades.

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

Valor que indica el retraso de la muestra más allá de su tiempo de espera, en unidades de tiempo de referencia.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tiempo de INTERMARCO, en unidades de tiempo de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




