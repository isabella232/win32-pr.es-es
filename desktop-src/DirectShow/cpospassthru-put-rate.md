---
description: El método put \_ Rate establece la velocidad de reproducción. Este método implementa el método IMediaPosition::p ut \_ Rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: CPosPassThru.put_Rate método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070061"
---
# <a name="cpospassthruput_rate-method"></a>Método CPosPassThru.put \_ Rate

El `put_Rate` método establece la velocidad de reproducción. Este método implementa el método [**IMediaPosition::p ut \_ Rate.**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dRate* 
</dt> <dd>

Velocidad de reproducción. No debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ INVALIDARG si *dRate* es cero. De lo contrario, devuelve **el valor HRESULT** del pin conectado.

## <a name="remarks"></a>Observaciones

Las tasas negativas indican el juego inverso. No todos los medios admitirán la reproducción inversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




