---
description: El método IsEndOfStream consulta si se recibió la notificación de fin de secuencia.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Método CBaseRenderer.IsEndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50aab34fe73f617409ae3f1e33d132a45f8ea771722c42629d9f0e3df5ebb115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872315"
---
# <a name="cbaserendererisendofstream-method"></a>Método CBaseRenderer.IsEndOfStream

El método consulta si se recibió la notificación de fin `IsEndOfStream` de flujo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la [**marca CBaseRenderer::m \_ bEOS.**](cbaserenderer-m-beos.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




