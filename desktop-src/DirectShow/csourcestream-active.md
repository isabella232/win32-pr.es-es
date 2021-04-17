---
description: 'El método activo notifica al pin que el filtro está activo ahora. Este método invalida el método CBasePin:: active. Si el PIN está conectado, este método inicia el subproceso de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Método CSourceStream. Active (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690509"
---
# <a name="csourcestreamactive-method"></a>CSourceStream. Active (método)

El `Active` método notifica al pin que el filtro está activo ahora. Este método invalida el método [**CBasePin:: Active**](cbasepin-active.md) . Si el PIN está conectado, este método inicia el subproceso de streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El PIN ya está activo.<br/>  |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | No se pudo iniciar el subproceso.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




