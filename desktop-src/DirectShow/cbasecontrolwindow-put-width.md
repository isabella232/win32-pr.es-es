---
description: El método put \_ Width establece el ancho de la ventana.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: CBaseControlWindow.put_Width método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f32175fe2b86f3b05105f5627cf1e02b2509e25ee12cc415cd88ea2baba5536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635715"
---
# <a name="cbasecontrolwindowput_width-method"></a>Método CBaseControlWindow.put \_ Width

El `put_Width` método establece el ancho de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Width* 
</dt> <dd>

Nuevo ancho de ventana, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

La ventana tiene una posición en el escritorio. Esto se expresa en píxeles mediante cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a través de la izquierda, la parte superior, el ancho y el alto; esta es la convención que se usa en DirectShow. Todas las coordenadas se expresan en píxeles y el cambio de cualquier coordenada actualizará la ventana inmediatamente.

Al establecer las coordenadas izquierda o superior, la ventana se mueve hacia la izquierda o hacia arriba, respectivamente. estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana. Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




