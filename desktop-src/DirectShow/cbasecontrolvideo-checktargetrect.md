---
description: El método CheckTargetRect determina si un rectángulo de destino es válido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Método CBaseControlVideo.CheckTargetRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057325"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Método CBaseControlVideo.CheckTargetRect

El `CheckTargetRect` método determina si un rectángulo de destino es válido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntero al rectángulo de destino que se comprobará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ INVALIDARG si no es válido; de lo contrario, devuelve NOERROR (S \_ OK).

## <a name="remarks"></a>Comentarios

Esta función miembro determina si el rectángulo de destino solicitado es válido. Dado que el rectángulo de destino especifica una posición en el cliente lógico de la ventana, las coordenadas pueden ser negativas, aunque el ancho y alto generales no pueden ser cero o un valor negativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




