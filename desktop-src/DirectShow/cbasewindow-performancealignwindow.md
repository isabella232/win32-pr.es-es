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
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016473"
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

## <a name="remarks"></a>Comentarios

Este método alinea los bordes izquierdo y superior de la ventana con los límites DWORD, lo que puede mejorar el rendimiento. Si la ventana tiene un elemento primario, el método devuelve S \_ OK pero realiza la alineación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




