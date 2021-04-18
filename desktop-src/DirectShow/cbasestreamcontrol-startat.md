---
description: 'El método StartAt informa al pin Cuándo debe comenzar a entregar los datos. Este método implementa el método IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl. StartAt (Strmctl. h)
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
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660113"
---
# <a name="cbasestreamcontrolstartat-method"></a>CBaseStreamControl. StartAt (método)

El `StartAt` método informa al pin Cuándo debe comenzar a entregar los datos. Este método implementa el método [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

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

Puntero a un valor de [**\_ hora de referencia**](reference-time.md) que especifica cuándo debe comenzar a entregar los datos el código PIN.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica un valor que se enviará junto con la notificación de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




