---
description: Lee los datos del filtro de la secuencia especificada.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670997"
---
# <a name="cpersiststreamreadfromstream-method"></a>CPersistStream. ReadFromStream, método

Lee los datos del filtro de la secuencia especificada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStream* 
</dt> <dd>

Puntero a una interfaz **IStream** desde la que se leerán los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto. La clase derivada debe devolver un valor **HRESULT** válido.

## <a name="remarks"></a>Observaciones

La versión predeterminada no es nada; se puede invalidar para leer datos específicos de la clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




