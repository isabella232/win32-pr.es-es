---
description: 'Método CTransformInputPin.SetMediaType: el método SetMediaType establece el tipo de medio para la conexión.'
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Método CTransformInputPin.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9af7310dbbf8830d7469c1a72ae43b946f1fbc69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095004"
---
# <a name="ctransforminputpinsetmediatype-method"></a>Método CTransformInputPin.SetMediaType

El `SetMediaType` método establece el tipo de medio para la conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Mt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::SetMediaType.**](cbasepin-setmediatype.md) Llama al método [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) del filtro para informar al filtro.

El pin debe comprobar que el tipo de medio es aceptable antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




