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
ms.openlocfilehash: ddd064934eea6ef2c88a4304466b15811910e8e352041e7242c75650dd54b2a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812785"
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
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Success<br/>            |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Índice fuera del intervalo<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::GetMediaType.**](cbasepin-getmediatype.md) Si el pin de entrada del filtro no está conectado, el método devuelve VFW \_ S \_ NO MORE \_ \_ ITEMS. De lo contrario, llama al método [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) del filtro para recuperar el tipo de medio. El **método CTransformFilter::GetMediaType** es virtual puro; La clase derivada del filtro debe invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




