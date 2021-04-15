---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661316"
---
# <a name="ctransforminputpinreceive-method"></a>CTransformInputPin. Receive (método)

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

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El PIN se está vaciando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) del PIN, que comprueba el estado de streaming del PIN y comprueba los cambios de formato en el tipo de medio. A continuación, llama al método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) del filtro, que procesa el ejemplo y lo entrega hacia abajo.

Si el filtro necesita tener acceso al ejemplo después de que este método devuelva, debe contener un recuento de referencias llamando al método **IUnknown:: AddRef** en el ejemplo. Por ejemplo, algunos filtros del descodificador necesitan el ejemplo actual para descodificar el ejemplo siguiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




