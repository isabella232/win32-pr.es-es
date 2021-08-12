---
description: El método OnRenderEnd realiza el suavizado para los casos en los que el tiempo de representación varía debido a interrupciones.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Método CBaseVideoRenderer.OnRenderEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d622ec62b27ae2e85eb9bef37516c82acbb17e03bef9a51b161edacd0b95c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658707"
---
# <a name="cbasevideorendereronrenderend-method"></a>Método CBaseVideoRenderer.OnRenderEnd

El método realiza el suavizado para los casos en los que el `OnRenderEnd` tiempo de representación varía debido a interrupciones.

## <a name="syntax"></a>Sintaxis


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero al ejemplo de medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar a esta función miembro justo después de dibujar una imagen.

Esta función miembro invalida [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




