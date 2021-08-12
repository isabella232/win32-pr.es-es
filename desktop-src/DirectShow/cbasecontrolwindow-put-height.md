---
description: El método put \_ Height establece el alto de la ventana.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: CBaseControlWindow.put_Height método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34774d366858e9c9bbe9ce5b02e897453bca21b9bd07d9eb11c60ac8313d33e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660042"
---
# <a name="cbasecontrolwindowput_height-method"></a>CBaseControlWindow.put \_ Height (método)

El `put_Height` método establece el alto de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Height* 
</dt> <dd>

Nuevo alto de la ventana, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

La ventana tiene una posición en el escritorio. Esto se expresa en píxeles mediante cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a través de la izquierda, la parte superior, el ancho y el alto; esta es la convención que se usa en DirectShow. Todas las coordenadas se expresan en píxeles y al cambiar cualquier coordenada se actualizará la ventana inmediatamente.

Al establecer las coordenadas izquierda o superior, la ventana se mueve hacia la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana. Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




