---
description: El método SetSourceRect establece el rectángulo de vídeo de origen actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de origen.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Método CBaseControlVideo.SetSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974045"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>Método CBaseControlVideo.SetSourceRect

El `SetSourceRect` método establece el rectángulo de vídeo de origen actual (virtual puro). Se trata de una función miembro interna a la que se llama cuando cambia el rectángulo de origen.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntero al rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Las clases derivadas deben invalidar esta función miembro para saber cuándo cambia el rectángulo de origen. Se llama desde las siguientes funciones miembro.

-   [**CBaseControlVideo::SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)
-   [**CBaseControlVideo::put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo,**](cbasecontrolvideo.md)m pRenderer contiene un objeto de una clase derivada de CBaseVideoRenderer y el miembro de datos m DrawImage, definido en la clase derivada, contiene un objeto \_ [](cbasevideorenderer.md) \_ [**CDrawImage.**](cdrawimage.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




