---
description: El método CheckMediaType determina si el pin acepta un tipo de medio específico. Este método implementa el método CBasePin::CheckMediaType virtual puro.
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Método CSourceStream.CheckMediaType (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb900d4de448b59eadb4cfd4de28aebf3ac07845fff6a2769c003d37cac846a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633935"
---
# <a name="csourcestreamcheckmediatype-method"></a>Método CSourceStream.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico. Este método implementa el método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Este pin admite este tipo de medio.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | El pin no admite este tipo de medio.<br/> |



 

## <a name="remarks"></a>Comentarios

De forma predeterminada, el pin admite un único tipo de medio. Este método recupera el tipo admitido llamando a la versión de parámetro único del método [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) y lo compara con el tipo propuesto. Si el pin admite más de un tipo de medio, invalide este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




