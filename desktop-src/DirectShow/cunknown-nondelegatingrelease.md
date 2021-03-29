---
description: 'Disminuye el recuento de referencias en el objeto. Este método implementa el método INonDelegatingUnknown:: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown. NonDelegatingRelease (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680876"
---
# <a name="cunknownnondelegatingrelease-method"></a>CUnknown. NonDelegatingRelease, método

Disminuye el recuento de referencias en el objeto. Este método implementa el método **INonDelegatingUnknown:: NonDelegatingRelease** .

## <a name="syntax"></a>Sintaxis


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de referencias.

## <a name="remarks"></a>Observaciones

Cuando el recuento de referencias llega a cero, el objeto se elimina a sí mismo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




