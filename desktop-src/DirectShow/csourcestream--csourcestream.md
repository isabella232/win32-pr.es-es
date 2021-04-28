---
description: 'Destructor CSourceStream.~CSourceStream: método destructor.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Destructor CSourceStream.~CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085213"
---
# <a name="csourcestreamcsourcestream-destructor"></a>Destructor CSourceStream.~CSourceStream

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CSourceStream();
```



## <a name="remarks"></a>Comentarios

El destructor quita automáticamente el pin del filtro propietario mediante una llamada [**a CSource::RemovePin**](csource-removepin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




