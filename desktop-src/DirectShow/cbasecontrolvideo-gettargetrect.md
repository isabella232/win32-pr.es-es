---
description: El método GetTargetRect recupera el rectángulo de destino. Se trata de una función miembro auxiliar interna.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Método CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670811"
---
# <a name="cbasecontrolvideogettargetrect-method"></a>CBaseControlVideo. GetTargetRect, método

El `GetTargetRect` método recupera el rectángulo de destino. Se trata de una función miembro auxiliar interna.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntero al rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro se debe invalidar en la clase derivada para devolver el rectángulo de destino mantenido por el representador de vídeo. Se llama desde las siguientes funciones miembro de [**CBaseControlVideo**](cbasecontrolvideo.md) .

-   [**CBaseControlVideo::GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)
-   [**CBaseControlVideo::p UT \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo:: get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)
-   [**CBaseControlVideo::p UT \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo:: get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)
-   [**CBaseControlVideo::p UT \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo:: get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)
-   [**CBaseControlVideo::p UT \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)
-   [**CBaseControlVideo:: get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




