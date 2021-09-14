---
description: El método PerformanceAlignWindow alinea la posición de la ventana con los límites DWORD para obtener el máximo rendimiento.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Método CBaseWindow.PerformanceAlignWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973909"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Método CBaseWindow.PerformanceAlignWindow

El `PerformanceAlignWindow` método alinea la posición de la ventana con los **límites DWORD** para obtener el máximo rendimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método alinea los bordes izquierdo y superior de la ventana con los límites DWORD, lo que puede mejorar el rendimiento. Si la ventana tiene un elemento primario, el método devuelve S \_ OK pero realiza la alineación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




