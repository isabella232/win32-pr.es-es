---
description: El método Receive recibe el siguiente ejemplo multimedia en la secuencia.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671844"
---
# <a name="cbaserendererreceive-method"></a>CBaseRenderer. Receive (método)

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

El PIN de entrada llama a este método cuando recibe un ejemplo del filtro de nivel superior.

Si el filtro se está ejecutando, este método realiza los siguientes pasos:

1.  Programa el ejemplo para la representación ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).
2.  Espera la hora programada ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Representa el ejemplo ([**CBaseRenderer:: Render**](cbaserenderer-render.md)).
4.  Libera el ejemplo ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Si el filtro está en pausa, el método realiza los pasos siguientes:

1.  Notifica a la clase derivada que hay un ejemplo disponible ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Espera la hora programada.
3.  Representa el ejemplo.
4.  Libera el ejemplo.

Mientras está en pausa, el método espera en el paso 2 hasta que el filtro cambia a un estado de ejecución. En ese momento, el filtro programa el ejemplo.

En la clase base, el método **OnReceiveFirstSample** no hace nada. La clase derivada puede invalidarla. Por ejemplo, cuando se pausa un representador de vídeo, muestra el primer ejemplo como imagen fija.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




