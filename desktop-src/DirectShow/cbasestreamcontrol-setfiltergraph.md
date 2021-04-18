---
description: El método SetFilterGraph especifica el receptor de eventos para los eventos de control de flujo.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Método CBaseStreamControl. SetFilterGraph (Strmctl. h)
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
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660115"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>CBaseStreamControl. SetFilterGraph, método

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

Puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) del administrador de gráficos de filtro, o **null** cuando el filtro deja el gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a este método desde dentro del método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro. La clase **CBaseStreamControl** usa la interfaz **IMediaEventSink** para enviar eventos de detención de control de [**flujo de EC \_ \_ \_ iniciado**](ec-stream-control-started.md) y de [**\_ \_ control \_ de flujo de EC**](ec-stream-control-stopped.md) .

Si el filtro se deriva de **CBaseFilter**, llame primero al método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , que establece la variable miembro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . Después, pase **m \_ pSink** al `SetFilterGraph` método. Tenga en cuenta que **m \_ PSink** es **null** cuando el filtro sale del gráfico, que es correcto.

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
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




