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
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261487"
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

 

 




