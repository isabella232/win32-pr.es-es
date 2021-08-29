---
description: El método \_ get PrerollTime recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el método IMediaPosition::get \_ PrerollTime.
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: CPosPassThru.get_PrerollTime método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8323849ddc8f6c4777df1d5a73c84c4c99f51c60b6c76cc81631f0869ed629b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073559"
---
# <a name="cpospassthruget_prerolltime-method"></a>Método PrerollTime de CPosPassThru.get \_

El `get_PrerollTime` método recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el [**método IMediaPosition::get \_ PrerollTime.**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de inscripción previa, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




