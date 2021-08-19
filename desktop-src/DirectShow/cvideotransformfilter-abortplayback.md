---
description: El método AbortPlayback se usa para señalar un error de streaming. Envía un evento EC ERRORABORT al Administrador de filtros Graph y envía una notificación de fin de \_ flujo de bajada.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Método CVideoTransformFilter.AbortPlayback (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821940"
---
# <a name="cvideotransformfilterabortplayback-method"></a>CVideoTransformFilter.AbortPlayback (método)

El `AbortPlayback` método se usa para señalar un error de streaming. Envía un evento [**\_ EC ERRORABORT**](ec-errorabort.md) al Administrador de filtros Graph y envía una notificación de fin de flujo de bajada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*h* 
</dt> <dd>

**Valor HRESULT** de la operación que ha dado error. Este valor se usa como primer parámetro de evento para el evento \_ ERRORABORT de EC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del *parámetro hr.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




