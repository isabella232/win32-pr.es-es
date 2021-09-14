---
description: 'Método CTransformOutputPin.SetMediaType: el método SetMediaType establece el tipo de medio para la conexión.'
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Método CTransformOutputPin.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255327"
---
# <a name="ctransformoutputpinsetmediatype-method"></a>Método CTransformOutputPin.SetMediaType

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

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBasePin::SetMediaType.**](cbasepin-setmediatype.md) Llama al método [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) del filtro para informar al filtro.

El pin debe comprobar que el tipo de medio es aceptable antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




