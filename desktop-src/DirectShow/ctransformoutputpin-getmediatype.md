---
description: 'Método CTransformOutputPin.GetMediaType: el método GetMediaType recupera un tipo de medio preferido, por valor de índice.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin.GetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255357"
---
# <a name="ctransformoutputpingetmediatype-method"></a>Método CTransformOutputPin.GetMediaType

El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice de base cero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                            | Descripción                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto<br/>            |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Índice fuera del intervalo<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBasePin::GetMediaType.**](cbasepin-getmediatype.md) Si el pin de entrada del filtro no está conectado, el método devuelve VFW \_ S \_ NO MORE \_ \_ ITEMS. De lo contrario, llama al método [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) del filtro para recuperar el tipo de medio. El **método CTransformFilter::GetMediaType** es virtual puro; La clase derivada del filtro debe invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




