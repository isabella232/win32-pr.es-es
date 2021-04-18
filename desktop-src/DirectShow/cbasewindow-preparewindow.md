---
description: El método PrepareWindow crea la ventana.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Método CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661232"
---
# <a name="cbasewindowpreparewindow-method"></a>CBaseWindow. PrepareWindow, método

El `PrepareWindow` método crea la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método después de crear el objeto. Este método realiza una contabilidad inicial y, a continuación, llama al método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) para crear la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




