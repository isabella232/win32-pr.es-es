---
description: El método GetSourceRect recupera el rectángulo de origen. Se trata de un método interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Método CBaseControlVideo.GetSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057055"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Método CBaseControlVideo.GetSourceRect

El `GetSourceRect` método recupera el rectángulo de origen. Se trata de un método interno.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntero al rectángulo de origen recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro se debe invalidar en la clase derivada para devolver el rectángulo de origen que mantiene el representador de vídeo. Se llama desde las siguientes [**funciones miembro CBaseControlVideo.**](cbasecontrolvideo.md)

-   [**CBaseControlVideo::GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)
-   [**CBaseControlVideo::put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**CBaseControlVideo::put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**CBaseControlVideo::put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**CBaseControlVideo::put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**CBaseControlVideo::get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)

En el ejemplo siguiente se muestra una implementación de esta función en una clase derivada.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



En este ejemplo, CVideoText es una clase derivada de [**CBaseControlVideo,**](cbasecontrolvideo.md)m pRenderer contiene un objeto de una clase derivada de CBaseVideoRenderer y el miembro de datos m DrawImage, definido en la clase derivada, contiene un objeto \_ [](cbasevideorenderer.md) \_ [**CDrawImage.**](cdrawimage.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




