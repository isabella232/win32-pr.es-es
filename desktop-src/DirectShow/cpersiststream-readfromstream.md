---
description: Lee los datos del filtro de la secuencia dada.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream.ReadFromStream (Pstream.h)
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
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073649"
---
# <a name="cpersiststreamreadfromstream-method"></a>CPersistStream.ReadFromStream (método)

Lee los datos del filtro de la secuencia dada.

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

Puntero a una **interfaz IStream** desde la que se leerán los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK. La clase derivada debe devolver un valor **HRESULT** válido.

## <a name="remarks"></a>Comentarios

La versión predeterminada no lee nada; se puede invalidar para leer datos específicos de la clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 




