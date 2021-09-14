---
description: El método CheckReady consulta si se ha completado una transición de estado.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Método CBaseRenderer.CheckReady (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161632"
---
# <a name="cbaserenderercheckready-method"></a>Método CBaseRenderer.CheckReady

El `CheckReady` método consulta si se ha completado una transición de estado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la transición de estado se ha completado o **FALSE** si el filtro sigue transfiriendo a un estado nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer::Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




