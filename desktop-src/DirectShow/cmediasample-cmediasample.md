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
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634695"
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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




