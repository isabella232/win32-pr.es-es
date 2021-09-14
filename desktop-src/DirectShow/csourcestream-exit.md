---
description: El método Exit indica al subproceso de streaming que se debe salir.
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
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072238"
---
# <a name="csourcestreamexit-method"></a>Método CSourceStream.Exit

El `Exit` método indica al subproceso de streaming que se debe salir.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ UNEXPECTED.

## <a name="remarks"></a>Observaciones

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

 

 




