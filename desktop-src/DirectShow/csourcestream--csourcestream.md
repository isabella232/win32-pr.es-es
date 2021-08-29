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
ms.openlocfilehash: a2e5fb1a09fe089df7d90846e25870a2c1e42987c07361809d958d303f257fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073359"
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
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




