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
ms.openlocfilehash: 376c2b292b0bdba9a79593c8264ecce17b916a88cfd49407638d637d1fbda6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767845"
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



 

## <a name="remarks"></a>Comentarios

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

 

 




