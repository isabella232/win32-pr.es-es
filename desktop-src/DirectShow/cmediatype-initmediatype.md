---
description: El método InitMediaType inicializa el tipo de medio.
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: CMediaType.Inimétodo tMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3402350a3b87f56bb03d3770983fdc024883b0695fa09ec7a03dc4c65c780882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156365"
---
# <a name="cmediatypeinitmediatype-method"></a>CMediaType.Inimétodo tMediaType

El `InitMediaType` método inicializa el tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
void InitMediaType();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método pone a cero la memoria del objeto, establece la propiedad fixed-sample-size en **TRUE** y establece el tamaño de la muestra en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




