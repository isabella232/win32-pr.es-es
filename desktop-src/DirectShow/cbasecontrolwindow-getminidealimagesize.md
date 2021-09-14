---
description: El método GetMinIdealImageSize recupera el tamaño de imagen ideal mínimo.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Método CBaseControlWindow.GetMinIdealImageSize (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974002"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>Método CBaseControlWindow.GetMinIdealImageSize

El `GetMinIdealImageSize` método recupera el tamaño de imagen ideal mínimo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho ideal mínimo, en píxeles.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto ideal mínimo, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Varios representadores tienen restricciones de rendimiento en cuanto al tamaño de las imágenes que pueden mostrar. Aunque seguirán funcionando correctamente cuando se les solicite para mostrar imágenes mayores que el máximo especificado, los representadores pueden designar los tamaños ideales mínimo y máximo a través de la interfaz [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Solo se puede llamar a esta interfaz cuando el gráfico de filtros está en pausa o en ejecución, porque no es hasta entonces cuando se asignan recursos y el representador puede reconocer sus restricciones. Si no existen restricciones, el representador rellena los parámetros *pWidth* y *pHeight* con las dimensiones de vídeo nativas y devuelve S \_ FALSE. Si existen restricciones, se introducen el ancho y el alto restringidos, y la función miembro devuelve S \_ OK.

Las dimensiones se aplican al tamaño del vídeo de destino y no al tamaño general de la ventana. Por lo tanto, al calcular el tamaño de la ventana que se establece, debe tener en cuenta los estilos de ventana actuales (por ejemplo, WS \_ CAPTION y WS \_ BORDER).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




