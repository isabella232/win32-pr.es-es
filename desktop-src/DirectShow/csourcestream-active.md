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
ms.openlocfilehash: 427c0318bad4df810b29f3596e3a9516f8dbb73e97dd7e378c561bef28bf2f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073349"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




