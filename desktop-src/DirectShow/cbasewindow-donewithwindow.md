---
description: El método DoneWithWindow destruye la ventana.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow.DoneWithWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016673"
---
# <a name="cbasewindowdonewithwindow-method"></a>Método CBaseWindow.DoneWithWindow

El `DoneWithWindow` método destruye la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Llame a este método desde el método destructor del objeto derivado.

Si se llama a este método desde el mismo subproceso que creó la ventana, el método realiza las siguientes acciones:

-   Llama al [**método CBaseWindow::InactivateWindow,**](cbasewindow-inactivatewindow.md) que desactiva la ventana.
-   Llama al [**método CBaseWindow::UninitialiseWindow,**](cbasewindow-uninitialisewindow.md) que libera los recursos usados por la ventana.
-   Destruye la ventana.

Si el subproceso que llama no es el subproceso que creó la ventana, el método `DoneWithWindow` envía un mensaje privado "destroy" a la ventana. Cuando la ventana recibe este mensaje, llama `DoneWithWindow` a por sí misma. (Si [**CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) es **TRUE,** la ventana publica el mensaje).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




