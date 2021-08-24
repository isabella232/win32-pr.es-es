---
description: El método InactivateWindow inactiva la ventana. En la clase base, este método oculta la ventana.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Método CBaseWindow.InactivateWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cf175a55ab5739b0fa171fe4c9553d3691be82d71b38fd5eb480d6e28043440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567465"
---
# <a name="cbasewindowinactivatewindow-method"></a>Método CBaseWindow.InactivateWindow

El `InactivateWindow` método inactiva la ventana. En la clase base, este método oculta la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La ventana ya está inactiva.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




