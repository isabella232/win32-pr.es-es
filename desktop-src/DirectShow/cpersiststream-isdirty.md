---
description: Indica si el objeto ha cambiado desde que se guardó por última vez en su secuencia actual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream.IsDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062414"
---
# <a name="cpersiststreamisdirty-method"></a>Método CPersistStream.IsDirty

Indica si el objeto ha cambiado desde que se guardó por última vez en su secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el filtro necesita guardarse y S FALSE si no necesita \_ guardar.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el **método IPersistStream::IsDirty.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 




