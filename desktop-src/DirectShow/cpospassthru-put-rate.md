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
ms.openlocfilehash: 90c89c9730ee057bea3bc776f551061c0e828385fe3c6ae054f4161bdb705ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565514"
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

## <a name="remarks"></a>Comentarios

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

 

 




