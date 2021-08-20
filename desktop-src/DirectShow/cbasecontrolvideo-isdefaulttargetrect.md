---
description: El método IsDefaultTargetRect determina si el representador usa el rectángulo de destino predeterminado (virtual puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Método CBaseControlVideo.IsDefaultTargetRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c11d5b99610ff88a9e5f4088aa47efdcd8f3d9d676f0b17fad4d8e316324e807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955244"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Método CBaseControlVideo.IsDefaultTargetRect

El `IsDefaultTargetRect` método determina si el representador usa el rectángulo de destino predeterminado (virtual puro).

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el representador usa el destino predeterminado; de lo contrario, devuelve S \_ FALSE.

## <a name="remarks"></a>Comentarios

Esta función miembro debe implementarse en la clase derivada. La llama la función [**miembro CBaseControlVideo::IsUsingDefaultDestination.**](cbasecontrolvideo-isusingdefaultdestination.md)

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo,**](cbasecontrolvideo.md)m pRenderer contiene un objeto de una clase derivada de CBaseVideoRenderer y el miembro de datos m DrawImage, definido en la clase derivada, contiene un objeto \_ [](cbasevideorenderer.md) \_ [**CDrawImage.**](cdrawimage.md) El miembro de datos m mtIn, también definido en la clase derivada, contiene un objeto CMediaType con el tipo de medio \_ de la patilla de entrada. [](cmediatype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




