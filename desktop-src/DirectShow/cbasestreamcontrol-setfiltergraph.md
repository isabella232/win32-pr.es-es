---
description: El método SetFilterGraph especifica el receptor de eventos para los eventos de control de flujo.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Método CBaseStreamControl.SetFilterGraph (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502645"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Método CBaseStreamControl.SetFilterGraph

El `SetFilterGraph` método especifica el receptor de eventos para los eventos de control de flujo.

## <a name="syntax"></a>Sintaxis


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSink* 
</dt> <dd>

Puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) del Administrador de gráficos de filtros o **NULL** cuando el filtro sale del gráfico de filtros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Llame a este método desde dentro del método [**IBaseFilter::JoinFilterGraph del**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) filtro. La **clase CBaseStreamControl usa** la interfaz **IMediaEventSink** para enviar eventos [**EC STREAM CONTROL \_ \_ \_ STARTED**](ec-stream-control-started.md) y [**EC STREAM CONTROL \_ \_ \_ STOPPED.**](ec-stream-control-stopped.md)

Si el filtro deriva de **CBaseFilter,** llame primero al método [**CBaseFilter::JoinFilterGraph,**](cbasefilter-joinfiltergraph.md) que establece la variable miembro [**CBaseFilter::m \_ pSink.**](cbasefilter-m-psink.md) A continuación, **\_ pase m pSink** al `SetFilterGraph` método . Tenga en **cuenta que m \_ pSink** es **NULL** cuando el filtro sale del gráfico, lo que es correcto.

## <a name="examples"></a>Ejemplos


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




