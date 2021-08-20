---
description: El método Set establece el tipo de medio de otro tipo de medio.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: 'Método CMediaType.Set (Mtype.h): parámetro mtype [ref]'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 350e88cefa7c0f5f6946218d220fcad4a118cf53e203a68eeb9f75c0d0eace1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156068"
---
# <a name="cmediatypeset-method-mtypeh"></a>Método CMediaType.Set (Mtype.h)

El `Set` método establece el tipo de medio de otro tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Referencia a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método copia todo el tipo de medio de *mtype*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




