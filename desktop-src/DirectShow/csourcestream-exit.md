---
description: El método Exit indica al subproceso de streaming que se cierre.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Método CSourceStream.Exit (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2c1c0de67eaa1067a4c72f3500674dddef65ddbb11af1b520973120d2df3c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687435"
---
# <a name="csourcestreamexit-method"></a>Método CSourceStream.Exit

El `Exit` método indica al subproceso de streaming que se cierre.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ UNEXPECTED.

## <a name="remarks"></a>Comentarios

El [**método CSourceStream::Inactive**](csourcestream-inactive.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




