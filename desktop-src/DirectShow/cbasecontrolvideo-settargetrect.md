---
description: El método SetTargetRect establece el rectángulo de destino actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de destino.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Método CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661207"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>CBaseControlVideo. SetTargetRect, método

El `SetTargetRect` método establece el rectángulo de destino actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de destino.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetTargetRect(
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

Las clases derivadas deben invalidar esto para saber cuándo cambia el rectángulo de destino. Se llama desde las siguientes funciones miembro.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo::p UT \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo::p UT \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo::p UT \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo::p UT \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
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

 

 




