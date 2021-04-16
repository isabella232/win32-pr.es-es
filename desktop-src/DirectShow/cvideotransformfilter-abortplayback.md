---
description: El método AbortPlayback se usa para indicar un error de streaming. Envía un \_ evento ERRORABORT de EC al administrador de gráficos de filtro y envía una notificación de final de secuencia de nivel inferior.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Método CVideoTransformFilter. AbortPlayback (Vtrans. h)
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
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678929"
---
# <a name="cvideotransformfilterabortplayback-method"></a>CVideoTransformFilter. AbortPlayback, método

El `AbortPlayback` método se usa para indicar un error de streaming. Envía un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) al administrador de gráficos de filtro y envía una notificación de final de secuencia de nivel inferior.

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

Valor **HRESULT** de la operación en la que se produjo un error. Este valor se usa como el primer parámetro de evento para el \_ evento ERRORABORT de EC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del parámetro *HR* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




