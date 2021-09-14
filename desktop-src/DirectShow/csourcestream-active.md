---
description: El método Active notifica al pin que el filtro ahora está activo. Este método invalida el método CBasePin::Active. Si el pin está conectado, este método inicia el subproceso de streaming.
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Método CSourceStream.Active (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072251"
---
# <a name="csourcestreamactive-method"></a>Método CSourceStream.Active

El `Active` método notifica al pin que el filtro ahora está activo. Este método invalida el [**método CBasePin::Active.**](cbasepin-active.md) Si el pin está conectado, este método inicia el subproceso de streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El pin ya está activo.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | No se pudo iniciar el subproceso.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




