---
description: El método RemovePin quita un pin especificado del filtro. El método no elimina el pin.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Método CSource.RemovePin (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070026"
---
# <a name="csourceremovepin-method"></a>Método CSource.RemovePin

El `RemovePin` método quita un pin especificado del filtro. El método no elimina el pin.

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

Puntero al [**objeto CSourceStream**](csourcestream.md) que implementa el pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El filtro no contiene este pin.<br/> |



 

## <a name="remarks"></a>Observaciones

El método destructor llama a este método para quitar el pin de salida del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




