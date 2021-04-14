---
description: El método GetDestinationPosition recupera el rectángulo de destino en una operación atómica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Método CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661407"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>CBaseControlVideo. GetDestinationPosition, método

El `GetDestinationPosition` método recupera el rectángulo de destino en una operación atómica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDestinationPosition(
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

Puntero a la coordenada izquierda del rectángulo de destino.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntero en la coordenada superior del rectángulo de destino.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntero al ancho del rectángulo de destino.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto del rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.



| Código devuelto                                                                                           | Descripción                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error.<br/>                                                              |
| <dl> <dt>**\_puntero E**</dt> </dl>             | Argumento de puntero **nulo** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | No se puede realizar la operación porque los PIN no están conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Correcto.<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

Esta función miembro se puede usar en lugar de llamadas independientes a las funciones miembro [**CBaseControlVideo:: get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo:: get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo:: get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)y [**CBaseControlVideo:: get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) . Una aplicación puede cambiar los rectángulos de origen y de destino para el vídeo a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . El rectángulo de origen afecta a qué sección del origen de vídeo nativo aparecerá en la pantalla. el rectángulo de destino afecta al lugar en el que aparecerá el vídeo cuando se reproduzca. El rectángulo de destino es relativo al área cliente de la ventana en la que se reproduce. La esquina superior izquierda de la ventana es la coordenada (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




