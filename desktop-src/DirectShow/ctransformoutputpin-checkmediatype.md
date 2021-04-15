---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661313"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>CTransformOutputPin. CheckMediaType, método

El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El PIN de entrada del filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro. El método genera un error si el PIN de entrada del filtro no está conectado. De lo contrario, llama al método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) del filtro, que también es virtual puro. La clase derivada del filtro debe implementar **CheckTransform**, que determina si el tipo de medio de salida propuesto es compatible con el tipo de medio de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




