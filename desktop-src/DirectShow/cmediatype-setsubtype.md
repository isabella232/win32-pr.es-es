---
description: El método SetSubtype especifica el subtipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Método CMediaType.SetSubtype (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566375"
---
# <a name="cmediatypesetsubtype-method"></a>Método CMediaType.SetSubtype

El `SetSubtype` método especifica el subtipo.

## <a name="syntax"></a>Sintaxis


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psubtype* 
</dt> <dd>

Puntero a un **GUID** que especifica el subtipo.

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

 

 




