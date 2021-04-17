---
description: El método CheckStreamState determina si se debe entregar o descartar un ejemplo multimedia.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Método CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660397"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>CBaseStreamControl. CheckStreamState, método

El `CheckStreamState` método determina si se debe entregar o descartar un ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                       | Descripción                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**descartar el flujo \_**</dt> </dl> | Descartar este ejemplo.<br/> |
| <dl> <dt>**FLUJO \_ de flujos**</dt> </dl>    | Entregue este ejemplo.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método cuando el código PIN reciba un ejemplo. Entregue el ejemplo solo si el valor devuelto es flujo de flujo \_ . Si el valor devuelto es \_ DEScartando el flujo, descarte el ejemplo.

Si el PIN descarta cualquier ejemplo, debe marcar el siguiente ejemplo que ofrece como discontinuidad, llamando al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

Si el filtro implementa la interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) para contar el número de fotogramas que quita, no cuente un fotograma descartado como un fotograma quitado.

Cuando el valor devuelto está \_ DEScartando el flujo, el método se bloquea hasta que el tiempo de referencia alcanza la hora de inicio del ejemplo. Esto evita que el PIN descartará los ejemplos demasiado rápidamente. Si el filtro está en pausa, el tiempo de espera es infinito, hasta que el filtro se ejecute, detenga o vacíe los datos. (Los cambios de estado de filtro y la transmisión por secuencias se producen en subprocesos independientes, por lo que no produce ningún interbloqueo).

La enumeración **CBaseStreamControl:: StreamControlState** se define de la siguiente manera:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se da por supuesto que el PIN usa una variable miembro denominada m \_ fLastSampleDiscarded para realizar un seguimiento de las discontinuidades.


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




