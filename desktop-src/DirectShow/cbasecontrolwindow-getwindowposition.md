---
description: El método GetWindowPosition recupera las coordenadas actuales de la ventana.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow.GetWindowPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966735"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Método CBaseControlWindow.GetWindowPosition

El `GetWindowPosition` método recupera las coordenadas actuales de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntero a la coordenada izquierda, en coordenadas de pantalla.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntero a la coordenada superior, en coordenadas de pantalla.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho de la ventana, en coordenadas de pantalla.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto de la ventana, en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




