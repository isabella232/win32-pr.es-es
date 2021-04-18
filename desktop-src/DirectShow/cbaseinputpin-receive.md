---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Método CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660191"
---
# <a name="cbaseinputpinreceive-method"></a>CBaseInputPin. Receive (método)

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Receive(
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

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | El PIN se está vaciando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Argumento de puntero **nulo** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                             |
| <dl> <dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt> </dl>   | Se produjo un error en tiempo de ejecución.<br/>                      |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>     | El PIN está detenido.<br/>                             |



 

## <a name="remarks"></a>Observaciones

El PIN de salida ascendente llama a este método para proporcionar un ejemplo al pin de entrada. El PIN de entrada debe realizar una de las siguientes acciones:

-   Procese el ejemplo antes de volver.
-   Devuelva y procese el ejemplo en un subproceso de trabajo.
-   Rechace el ejemplo.

Si el PIN usa un subproceso de trabajo para procesar el ejemplo, agregue un recuento de referencias al ejemplo dentro de este método. Una vez que el método devuelve, el PIN ascendente libera el ejemplo. Cuando el recuento de referencias del ejemplo llega a cero, el ejemplo vuelve al asignador para reutilizarlo.

Este método es sincrónico y puede bloquearse. Si el método puede bloquearse, el método [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del PIN debe devolver s \_ correcto.

En la clase base, este método realiza los pasos siguientes:

1.  Llama al método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) para comprobar que el pin puede procesar los ejemplos ahora. Si no puede, por ejemplo, si se detiene el PIN, se produce un error en el método.
2.  Recupera las propiedades de ejemplo y comprueba si el formato ha cambiado (consulte a continuación).
3.  Si el formato ha cambiado, el método llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el nuevo formato es aceptable.
4.  Si el nuevo formato no es aceptable, el método llama al método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , envía un \_ evento ERRORABORT de EC y devuelve un código de error.
5.  Suponiendo que no haya errores, el método devuelve S \_ correcto.

Compruebe si hay un cambio de formato de la siguiente manera:

-   Si el ejemplo admite la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , compruebe el miembro **dwSampleFlags** de la estructura [**AM \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) . Si la \_ marca TYPECHANGED de ejemplo AM \_ está presente, el formato ha cambiado.
-   En caso contrario, si el ejemplo no es compatible con **IMediaSample2**, llame al método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) . Si el método devuelve un valor distinto de **null** , el formato ha cambiado.

En la clase base, este método no procesa el ejemplo. La clase derivada debe invalidar este método para realizar el procesamiento. (Lo que conlleva depende completamente del filtro). La clase derivada debe llamar al método de clase base para comprobar los errores descritos anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




