---
description: 'Método CTransformOutputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin.CheckMediaType (Transfrm.h)
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
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255387"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>CTransformOutputPin.CheckMediaType (método)

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.

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

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El pin de entrada del filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método implementa el método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro. Se produce un error en el método si el pin de entrada del filtro no está conectado. De lo contrario, llama al método [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) del filtro, que también es virtual puro. La clase derivada del filtro debe implementar **CheckTransform**, que determina si el tipo de medio de salida propuesto es compatible con el tipo de medio de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




