---
description: El método UninitialiseWindow libera los recursos de la ventana.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Método CBaseWindow.UninitialiseWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973906"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Método CBaseWindow.UninitialiseWindow

El `UninitialiseWindow` método libera los recursos de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método libera los recursos adquiridos por el [**método CBaseWindow::InitialiseWindow.**](cbasewindow-initialisewindow.md) El [**método CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




