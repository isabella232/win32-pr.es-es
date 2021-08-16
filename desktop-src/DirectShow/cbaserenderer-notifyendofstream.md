---
description: El método NotifyEndOfStream envía un evento EC \_ COMPLETE al administrador de gráficos de filtros.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: Método CBaseRenderer.NotifyEndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05504b2ca1520320777b93c1c066e91edd5135798e4710c6514dbe858737760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402816"
---
# <a name="cbaserenderernotifyendofstream-method"></a>Método CBaseRenderer.NotifyEndOfStream

El `NotifyEndOfStream` método envía un evento EC [**\_ COMPLETE**](ec-complete.md) al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::EndOfStream**](cbaserenderer-endofstream.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




