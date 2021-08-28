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
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108445"
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

Devuelve S \_ OK si el filtro necesita guardar y S FALSE si no necesita \_ guardar.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el **método IPersistStream::IsDirty.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 




