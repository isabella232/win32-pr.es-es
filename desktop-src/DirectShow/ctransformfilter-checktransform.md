---
description: El método CheckTransform comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Método CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660731"
---
# <a name="ctransformfilterchecktransform-method"></a>CTransformFilter. CheckTransform, método

El `CheckTransform` método comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de entrada.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Los tipos de medios son compatibles.<br/>     |
| <dl> <dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt> </dl> | Los tipos de medios no son compatibles.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase derivada debe implementar este método. Devuelve S \_ OK si el filtro puede aceptar ambos tipos de medios especificados o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




