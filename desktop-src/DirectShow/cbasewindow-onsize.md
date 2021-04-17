---
description: El método Datasize controla \_ los mensajes de tamaño de WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Método CBaseWindow. My size (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679181"
---
# <a name="cbasewindowonsize-method"></a>CBaseWindow. alsize (método)

El `OnSize` método controla \_ los mensajes de tamaño de WM.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Width* 
</dt> <dd>

Ancho del área cliente, en píxeles.

</dd> <dt>

*Height* 
</dt> <dd>

Alto del área cliente, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="remarks"></a>Observaciones

Este método almacena el nuevo ancho y alto. Para recuperar estos valores, llame a los métodos [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) y [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




