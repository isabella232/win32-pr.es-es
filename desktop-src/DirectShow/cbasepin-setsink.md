---
description: El método SetSink establece un administrador de calidad externo. Este método implementa el método IQualityControl::SetSink.
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin.SetSink (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e94dc561e378ab526eee04f82e0f54a90889ee4396996d96d01f6c8da8c34d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108635"
---
# <a name="cbasepinsetsink-method"></a>Método CBasePin.SetSink

El `SetSink` método establece un administrador de calidad externo. Este método implementa el [**método IQualityControl::SetSink.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piqc* 
</dt> <dd>

Puntero a la [**interfaz IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del administrador de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Llame a este método para redirigir los mensajes de control de calidad a un administrador de calidad externo. Para obtener más información, vea [Administración de control de calidad.](quality-control-management.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




