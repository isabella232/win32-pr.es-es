---
description: Escribe los datos del filtro en la secuencia especificada.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Método CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680368"
---
# <a name="cpersiststreamwritetostream-method"></a>CPersistStream. WriteToStream, método

Escribe los datos del filtro en la secuencia especificada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStream* 
</dt> <dd>

Puntero a una interfaz **IStream** que especifica la secuencia de destino de los datos del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto. La clase derivada debe devolver un valor **HRESULT** válido.

## <a name="remarks"></a>Observaciones

La versión predeterminada no escribe nada; se puede invalidar para escribir datos específicos de la clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




