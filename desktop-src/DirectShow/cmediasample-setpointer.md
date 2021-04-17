---
description: El método SetPointer establece el puntero en el búfer de memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Método CMediaSample. SetPointer (Amfilter. h)
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
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679075"
---
# <a name="cmediasamplesetpointer-method"></a>CMediaSample. SetPointer, método

El `SetPointer` método establece el puntero en el búfer de memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptr* 
</dt> <dd>

Puntero a un búfer de memoria asignado por el autor de la llamada, de tamaño *cBytes*.

</dd> <dt>

*cBytes* 
</dt> <dd>

Longitud del búfer, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método permite al asignador establecer un nuevo puntero para el ejemplo.

Este método no está disponible a través de la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . El objeto que crea el ejemplo puede tener acceso a este método (a través de **CMediaSample**), pero otros objetos no pueden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




