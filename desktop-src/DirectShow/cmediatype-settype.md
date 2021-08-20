---
description: El método SetType especifica el tipo principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Método CMediaType.SetType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37d035202d4674da11016620dc3c3d1ba3ab99f6ca514b9581f7dd2e4d9592d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954394"
---
# <a name="cmediatypesettype-method"></a>Método CMediaType.SetType

El `SetType` método especifica el tipo principal.

## <a name="syntax"></a>Sintaxis


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptype* 
</dt> <dd>

Puntero a un **GUID** que especifica el tipo principal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




