---
description: El método SetPointer establece el puntero al búfer de memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Método CMediaSample.SetPointer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af6747eb9ed39a973d795d8701fd9d7afd1b88e9d0b0db577de6a8e963b840bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634355"
---
# <a name="cmediasamplesetpointer-method"></a>Método CMediaSample.SetPointer

El `SetPointer` método establece el puntero al búfer de memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ptr* 
</dt> <dd>

Puntero a un búfer de memoria asignado por el autor de la llamada, de *tamaño cBytes*.

</dd> <dt>

*cBytes* 
</dt> <dd>

Longitud del búfer, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método permite al asignador establecer un nuevo puntero para el ejemplo.

Este método no está disponible a través de la [**interfaz IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) El objeto que crea el ejemplo puede tener acceso a este método (a través **de CMediaSample),** pero otros objetos no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




