---
description: El método put \_ Left establece la coordenada izquierda de la ventana.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: CBaseControlWindow.put_Left método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173858"
---
# <a name="cbasecontrolwindowput_left-method"></a>CBaseControlWindow.put \_ Left (método)

El `put_Left` método establece la coordenada izquierda de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Left* 
</dt> <dd>

Nueva coordenada izquierda, en píxeles.

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

 

 




