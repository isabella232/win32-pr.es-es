---
description: Determina si un rectángulo de origen es válido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Método CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660529"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>CBaseControlVideo. CheckSourceRect, método

Determina si un rectángulo de origen es válido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntero al rectángulo de origen que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ INVALIDARG si no es válido; en caso contrario, devuelve NoError (S \_ OK).

## <a name="remarks"></a>Observaciones

Esta función miembro comprueba que el rectángulo de origen solicitado no supera el vídeo de origen disponible. Las coordenadas izquierda y superior no pueden ser negativas y el ancho y el alto no pueden superar la parte derecha e inferior del vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




