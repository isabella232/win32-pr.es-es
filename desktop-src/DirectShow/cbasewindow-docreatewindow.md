---
description: El método DoCreateWindow crea la ventana.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCmétodo reateWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2502d1c07efbb5fa15c8113d11504b9a61a64321686e2b0e7e4939fabad7395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658229"
---
# <a name="cbasewindowdocreatewindow-method"></a>CBaseWindow.DoCmétodo reateWindow

El `DoCreateWindow` método crea la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

El [**método CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




