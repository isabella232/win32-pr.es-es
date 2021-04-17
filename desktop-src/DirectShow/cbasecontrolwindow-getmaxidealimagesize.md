---
description: El método GetMaxIdealImageSize recupera el tamaño de imagen máximo ideal.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Método CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660599"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a>CBaseControlWindow. GetMaxIdealImageSize, método

El `GetMaxIdealImageSize` método recupera el tamaño de imagen máximo ideal.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho máximo ideal, en píxeles.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto máximo ideal, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Varios representadores tienen restricciones de rendimiento en cuanto al tamaño de las imágenes que pueden mostrar. Aunque deberían seguir funcionando correctamente cuando se solicita que muestren imágenes mayores que el máximo especificado, los representadores pueden designar los tamaños máximo y mínimo ideales a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Solo se puede llamar a esta interfaz cuando el gráfico de filtros está en pausa o en ejecución, ya que no es hasta entonces se asignan los recursos y el representador puede reconocer sus restricciones. Si no existen restricciones, el representador rellena los parámetros *pWidth* y *pHeight* con las dimensiones de vídeo nativas y devuelve S \_ false. Si existen restricciones, se especifican el ancho y el alto restringidos, y la función miembro devuelve S \_ OK.

Las dimensiones se aplican al tamaño del vídeo de destino y no al tamaño total de la ventana. Por lo tanto, al calcular el tamaño de la ventana que se va a establecer, tenga en cuenta los estilos de ventana actuales (por ejemplo, WS \_ Caption y WS \_ Border).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




