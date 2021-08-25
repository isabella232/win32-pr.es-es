---
description: Se llama al método OnError si se produce un error durante el streaming. La clase derivada debe implementar este método.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Método CPullPin.OnError (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0d9873e2d327c424b2cd1ffda7112676f53399a63d2a9ca92dca1f50a02f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908885"
---
# <a name="cpullpinonerror-method"></a>Método CPullPin.OnError

Se `OnError` llama al método si se produce un error durante el streaming. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*h* 
</dt> <dd>

Especifica el valor **HRESULT** devuelto por el método que ha dado error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El objeto llama a este método cada vez que se produce un error que detiene el subproceso de extracción de datos. El filtro puede usar este método para recuperarse correctamente de los errores de streaming. En la mayoría de los casos, el error se devuelve desde el filtro ascendente, por lo que el filtro ascendente es responsable de notificarlo al Administrador de Graph. Si el error se produce dentro del [**método CPullPin::Receive,**](cpullpin-receive.md) el filtro debe enviar un [**evento EC \_ ERRORABORT.**](ec-errorabort.md) (Vea [**IMediaEventSink::Notify).**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




