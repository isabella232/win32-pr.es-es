---
description: El método GetReader devuelve un puntero a la interfaz IAsyncReader del pin de salida.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Método CPullPin.GetReader (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7880cba8e910c3da8ade049e18ae22e403c0c616246e4dfde94e587a1fcdeab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055005"
---
# <a name="cpullpingetreader-method"></a>Método CPullPin.GetReader

El `GetReader` método devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del pin de salida.

## <a name="syntax"></a>Sintaxis


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la [**interfaz IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

## <a name="remarks"></a>Comentarios

La interfaz devuelta tiene un recuento de referencias pendiente. El autor de la llamada debe liberar la interfaz .

El método no comprueba el valor del puntero de interfaz antes de llamar a **AddRef,** por lo que no llame a esto hasta que haya llamado correctamente al método [**CPullPin::Conectar.**](cpullpin-connect.md) De lo contrario, el puntero de interfaz podría ser **NULL** y llamar a **AddRef** producirá una excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




