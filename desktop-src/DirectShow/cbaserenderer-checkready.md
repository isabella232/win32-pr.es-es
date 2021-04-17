---
description: El método CheckReady consulta si se ha completado una transición de estado.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Método CBaseRenderer. CheckReady (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660760"
---
# <a name="cbaserenderercheckready-method"></a>CBaseRenderer. CheckReady, método

El `CheckReady` método consulta si se ha completado una transición de estado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la transición de estado está completa o **false** si el filtro sigue pasando a un nuevo estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer:: Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




