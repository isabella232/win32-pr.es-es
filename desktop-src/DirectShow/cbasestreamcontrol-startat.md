---
description: El método StartAt informa al pin cuándo empezar a entregar datos. Este método implementa el método IAMStreamControl::StartAt.
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl.StartAt (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40570933e7eed054694b2da927d71e077b86941aea816ff2ca6de5c91372b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814115"
---
# <a name="cbasestreamcontrolstartat-method"></a>Método CBaseStreamControl.StartAt

El `StartAt` método informa al pin cuándo empezar a entregar datos. Este método implementa el [**método IAMStreamControl::StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptStart* 
</dt> <dd>

Puntero a un [**valor REFERENCE \_ TIME**](reference-time.md) que especifica cuándo el pin debe empezar a entregar datos.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica un valor que se enviará junto con la notificación de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




