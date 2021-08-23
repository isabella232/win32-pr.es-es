---
description: El método get \_ Width recupera el ancho de ventana actual.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: CBaseControlWindow.get_Width método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3dff6e2a0929963f06c14aa8899b2a1d6a268db8f87b5067d2ed65f90964c803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768245"
---
# <a name="cbasecontrolwindowget_width-method"></a>CBaseControlWindow.get \_ Width (método)

El `get_Width` método recupera el ancho actual de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho de la ventana, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

La ventana tiene una posición en el escritorio. Esto se expresa en píxeles mediante cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a través de la izquierda, la parte superior, el ancho y el alto. esta es la convención que se usa en DirectShow. Todas las coordenadas se expresan en píxeles y al cambiar cualquier coordenada se actualizará la ventana inmediatamente.

Al establecer las coordenadas izquierdas o superiores, la ventana se mueve hacia arriba o hacia la izquierda, respectivamente. Estas coordenadas no tienen ningún efecto en el ancho y alto de la ventana. Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




