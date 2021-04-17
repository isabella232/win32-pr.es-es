---
description: El método SetDefaultSourceRect establece el rectángulo de vídeo de origen predeterminado (virtual puro). This en una función miembro interna a la que se llama cuando se restablece el rectángulo de origen.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Método CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671170"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>CBaseControlVideo. SetDefaultSourceRect, método

El `SetDefaultSourceRect` método establece el rectángulo de vídeo de origen predeterminado (virtual puro). This en una función miembro interna a la que se llama cuando se restablece el rectángulo de origen.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Las clases derivadas deben invalidar esto para restablecer el rectángulo de origen. Se llama desde [**CBaseControlVideo:: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md)y el miembro de \_ datos m DrawImage, definido en la clase derivada, contiene un objeto [**CDrawImage**](cdrawimage.md) . El \_ miembro de datos m mtIn, también definido en la clase derivada, contiene un objeto [**CMediaType**](cmediatype.md) con el tipo de medio del PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




