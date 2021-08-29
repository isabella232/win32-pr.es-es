---
description: El método CheckStreamState determina si se debe entregar o descartar un ejemplo multimedia.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Método CBaseStreamControl.CheckStreamState (Strmctl.h)
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
ms.openlocfilehash: 59c74f6933929b54be7e4933220358105f2dbe6d7be5f74db13be7c3092ffe17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537385"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>Método CBaseStreamControl.CheckStreamState

El método determina si se debe entregar o descartar un ejemplo `CheckStreamState` multimedia.

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

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                       | Descripción                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**DESCARTE \_ DE SECUENCIAS**</dt> </dl> | Descarte este ejemplo.<br/> |
| <dl> <dt>**FLUJO \_ DE FLUJO**</dt> </dl>    | Entregue este ejemplo.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método cuando el pin reciba un ejemplo. Entregue el ejemplo solo si el valor devuelto es STREAM \_ FLOWING. Si el valor devuelto es STREAM \_ DISCARDING, descarte el ejemplo.

Si el pin descarta alguna muestra, debe marcar el ejemplo siguiente que entrega como una discontinuidad, llamando al método [**IMediaSample::SetDiscontinuity.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)

Si el filtro implementa la interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) para contar cuántos fotogramas quita, no cuente un fotograma descartado como un fotograma descartado.

Cuando el valor devuelto es STREAM DISCARDING, el método se bloquea hasta que la \_ hora de referencia alcanza la hora de inicio del ejemplo. Esto evita que el pin descarte muestras demasiado rápidamente. Si el filtro está en pausa, el tiempo de espera es infinito, hasta que el filtro se ejecuta, detiene o vacía los datos. (Los cambios de estado de filtro y la transmisión por secuencias se hacen en subprocesos independientes, por lo que esto no provoca ningún interbloqueo).

La **enumeración CBaseStreamControl::StreamControlState** se define de la siguiente manera:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se supone que el pin usa una variable miembro denominada m fLastSampleDiscarded para realizar un \_ seguimiento de las discontinuidades.


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
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




