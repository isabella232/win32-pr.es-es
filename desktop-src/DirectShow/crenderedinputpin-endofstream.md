---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando de ejecución para el filtro. Este método implementa el método IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660746"
---
# <a name="crenderedinputpinendofstream-method"></a>CRenderedInputPin. EndOfStream, método

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando de ejecución para el filtro. Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Si el filtro se está ejecutando, este método envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro. De lo contrario, se establece una marca para que el \_ evento de finalización de EC se envíe cuando se ejecute el filtro siguiente. Vaciar el filtro borra la marca.

Debe invalidar este método para que contenga el bloqueo de streaming del PIN:


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



Además, si el filtro procesa llamadas de **recepción** de forma asincrónica, el PIN debe esperar para enviar el \_ evento de finalización de EC hasta que el filtro haya procesado todos los ejemplos pendientes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amextra. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




