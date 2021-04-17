---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680337"
---
# <a name="ctransforminputpinendofstream-method"></a>CTransformInputPin. EndOfStream, método

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | El PIN se está vaciando actualmente.<br/>       |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN de salida no está conectado.<br/> |
| <dl> <dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt> </dl> | Se produjo un error en tiempo de ejecución.<br/>       |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>   | El PIN está detenido.<br/>              |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CTransformFilter:: EndOfStream**](ctransformfilter-endofstream.md) del filtro para proporcionar la notificación de final de secuencia de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




