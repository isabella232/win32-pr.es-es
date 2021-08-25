---
description: 'Método CPosPassThru.SetRate: el método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking::SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Método CPosPassThru.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c411f2c342bd54f89ac85ad4275a05e9d7854908c1d8ba88b1181f34e56f57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909075"
---
# <a name="cpospassthrusetrate-method"></a>Método CPosPassThru.SetRate

El `SetRate` método establece la velocidad de reproducción. Este método implementa el [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRate(
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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




