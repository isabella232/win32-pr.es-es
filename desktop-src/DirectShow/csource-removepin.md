---
description: El método RemovePin quita un PIN especificado del filtro. El método no elimina el código PIN.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: CSource. RemovePin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661183"
---
# <a name="csourceremovepin-method"></a>CSource. RemovePin, método

El `RemovePin` método quita un PIN especificado del filtro. El método no elimina el código PIN.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStream* 
</dt> <dd>

Puntero al objeto [**CSourceStream**](csourcestream.md) que implementa el código PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | El filtro no contiene este pin.<br/> |



 

## <a name="remarks"></a>Observaciones

El método de destructor llama a este método para quitar el punto de conexión de salida del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSource**](csource.md)
</dt> </dl>

 

 




