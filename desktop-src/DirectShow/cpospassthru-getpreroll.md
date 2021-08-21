---
description: El método GetPreroll recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el método IMediaSeeking::GetPreroll.
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru.GetPreroll (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b34cd565d246f4401061834b21c005306633e72a6f24cc8367a222b5f3736c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954044"
---
# <a name="cpospassthrugetpreroll-method"></a>Método CPosPassThru.GetPreroll

El `GetPreroll` método recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el [**método IMediaSeeking::GetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de inscripción previa, en unidades del formato de hora actual.

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

 

 




