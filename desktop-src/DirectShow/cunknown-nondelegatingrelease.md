---
description: Disminuye el recuento de referencias en el objeto . Este método implementa el método INonDelegatingUnknown::NonDelegatingRelease.
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown.NonDelegatingRelease (Combase.h)
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
ms.openlocfilehash: 1ac5145e1776602c5bb358805c45ec271766fe918b7924d948e286ae32b31794
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821960"
---
# <a name="cunknownnondelegatingrelease-method"></a>CUnknown.NonDelegatingRelease (método)

Disminuye el recuento de referencias en el objeto . Este método implementa el **método INonDelegatingUnknown::NonDelegatingRelease.**

## <a name="syntax"></a>Sintaxis


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de referencias.

## <a name="remarks"></a>Comentarios

Cuando el recuento de referencias alcanza cero, el objeto se elimina a sí mismo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




