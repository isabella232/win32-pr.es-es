---
description: El método QueryAccept determina si el pin acepta un tipo de medio especificado. Este método implementa el método IPin::QueryAccept.
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Método CBasePin.QueryAccept (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74a179fd1a7f59dcf4e4d22eadf509db9b00cbe482d55e6a6755d7207de8079d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689005"
---
# <a name="cbasepinqueryaccept-method"></a>Método CBasePin.QueryAccept

El `QueryAccept` método determina si el pin acepta un tipo de medio especificado. Este método implementa el [**método IPin::QueryAccept.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio es aceptable. De lo contrario, devuelve S \_ FALSE.

## <a name="remarks"></a>Comentarios

En la clase base, este método delega en el [**método CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md) Si se produce un error **en CheckMediaType,** `QueryAccept` devuelve S \_ FALSE.

Este método no contiene la sección crítica del pin ([**CBasePin::m \_ pLock**](cbasepin-m-plock.md)). Si la clase derivada modifica dinámicamente el conjunto de tipos de medios aceptables, debe invalidar este método para contener la sección crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




