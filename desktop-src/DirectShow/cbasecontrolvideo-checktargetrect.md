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
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255603"
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

## <a name="remarks"></a>Observaciones

Esta función miembro determina si el rectángulo de destino solicitado es válido. Dado que el rectángulo de destino especifica una posición en el cliente lógico de la ventana, las coordenadas pueden ser negativas, aunque el ancho y alto generales no pueden ser cero o un valor negativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




