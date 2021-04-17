---
description: El método Set establece el tipo de medio desde otro tipo de medio.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType. set (mtype. h)
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
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670557"
---
# <a name="cmediatypeset-method-mtypeh"></a>Método CMediaType. set (mtype. h)

El `Set` método establece el tipo de medio desde otro tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtype* \[ CLI\]
</dt> <dd>

Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método copia el tipo de medio completo de *mtype*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




