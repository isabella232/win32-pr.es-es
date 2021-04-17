---
description: El \_ método put FullScreenMode establece el modo de pantalla completa del representador.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Método CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660626"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow. put \_ FullScreenMode (método)

El `put_FullScreenMode` método establece el modo de pantalla completa del representador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Modo de pantalla completa que se va a aplicar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . La implementación actual devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Observaciones

Un representador de vídeo que implementa un modo de pantalla completa debe reemplazar esta función miembro e implementar cualquier modo que admita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




