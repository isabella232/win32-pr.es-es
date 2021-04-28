---
description: 'Constructor CMediaSample.CMediaSample: método constructor.'
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Constructor CMediaSample.CMediaSample (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095443"
---
# <a name="cmediasamplecmediasample-constructor"></a>Constructor CMediaSample.CMediaSample

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

ignorado.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Puntero al objeto [**CBaseAllocator**](cbaseallocator.md) que creó este ejemplo.

</dd> <dt>

*Phr* 
</dt> <dd>

ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer de memoria asignado por el autor de la llamada, de longitud *de tamaño*.

</dd> <dt>

*length* 
</dt> <dd>

Longitud del búfer de memoria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La clase base no modifica el **valor HRESULT** pasado en el *parámetro phr.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




