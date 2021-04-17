---
description: 'El método SetSink establece un administrador de calidad externo. Este método implementa el método IQualityControl:: SetSink.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin. SetSink (Amfilter. h)
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
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660482"
---
# <a name="cbasepinsetsink-method"></a>CBasePin. SetSink, método

El `SetSink` método establece un administrador de calidad externo. Este método implementa el método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .

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

Puntero a la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del administrador de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Llame a este método para redirigir los mensajes de control de calidad a un administrador de calidad externo. Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




