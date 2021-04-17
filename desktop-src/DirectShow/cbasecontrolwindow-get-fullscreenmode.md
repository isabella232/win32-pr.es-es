---
description: El \_ método get FullScreenMode recupera el modo de pantalla completa actual.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Método CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671168"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>CBaseControlWindow. Get \_ FullScreenMode (método)

El `get_FullScreenMode` método recupera el modo de pantalla completa actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Puntero al modo de pantalla completa actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve E \_ NOTIMPL de forma predeterminada. Esto informa al distribuidor del complemento de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) de que este representador no implementa un representador de pantalla completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




