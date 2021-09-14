---
description: El método put StopTime establece la hora a la que se detendrá la \_ reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaPosition::p ut \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: CPosPassThru.put_StopTime método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070060"
---
# <a name="cpospassthruput_stoptime-method"></a>Método CPosPassThru.put \_ StopTime

El `put_StopTime` método establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el [**método IMediaPosition::p ut \_ StopTime.**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*llTime* 
</dt> <dd>

Tiempo de detenerse como **un valor** doble, en segundos.

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

 

 




