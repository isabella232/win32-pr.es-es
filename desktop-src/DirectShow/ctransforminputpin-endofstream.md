---
description: 'Método CTransformInputPin.EndOfStream: el método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin::EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin.EndOfStream (Transfrm.h)
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
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084983"
---
# <a name="ctransforminputpinendofstream-method"></a>Método CTransformInputPin.EndOfStream

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | El pin se está vacíando actualmente.<br/>       |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin de salida no está conectado.<br/> |
| <dl> <dt>**ERROR EN TIEMPO DE EJECUCIÓN DE VFW \_ E \_ \_**</dt> </dl> | Se produjo un error en tiempo de ejecución.<br/>       |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl>   | El pin se detiene.<br/>              |



 

## <a name="remarks"></a>Comentarios

Este método llama al método [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) del filtro para entregar la notificación de fin de flujo de bajada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




