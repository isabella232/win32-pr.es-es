---
description: El método EndOfStream notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando de ejecución para el filtro. Este método implementa el método IPin::EndOfStream.
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin.EndOfStream (Arendertra.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246681"
---
# <a name="crenderedinputpinendofstream-method"></a>Método CRenderedInputPin.EndOfStream

El método notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando `EndOfStream` de ejecución para el filtro. Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Si el filtro se está ejecutando, este método envía un [**evento EC \_ COMPLETE**](ec-complete.md) al administrador de Graph Manager. De lo contrario, establece una marca para que el evento \_ EC COMPLETE se envíe cuando se ejecute el filtro siguiente. Al vaciar el filtro, se borra la marca.

Debe invalidar este método para mantener el bloqueo de streaming del pin:


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



Además, si el filtro procesa las llamadas **receive** de forma asincrónica, el pin debe esperar para enviar el evento EC COMPLETE hasta que el filtro haya procesado \_ todas las muestras pendientes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Anicetra.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRenderedInputPin (clase)**](crenderedinputpin.md)
</dt> </dl>

 

 




