---
description: El método \_ put PrerollTime establece la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el método \_ PrerollTime IMediaPosition::p ut.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: CPosPassThru.put_PrerollTime método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825c3c584fc6db7eb9f94b4e8d01e003f5cf6c36ff8adac4041fd48f792ca858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909205"
---
# <a name="cpospassthruput_prerolltime-method"></a>Método PrerollTime de CPosPassThru.put \_

El `put_PrerollTime` método establece la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el [**método \_ PrerollTime IMediaPosition::p ut.**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*llTime* 
</dt> <dd>

Tiempo de inscripción previa, en segundos.

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

 

 




