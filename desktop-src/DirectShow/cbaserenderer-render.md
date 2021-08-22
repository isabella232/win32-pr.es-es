---
description: El método Render representa un ejemplo.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Método CBaseRenderer.Render (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 185baf6818d2022dbe7b64cfab888945e1a2405433eefa925d2de70dcca286e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016863"
---
# <a name="cbaserendererrender-method"></a>Método CBaseRenderer.Render

El `Render` método representa un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El filtro se detiene o *pMediaSample* es **NULL.**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                              |



 

## <a name="remarks"></a>Comentarios

Este método llama al método virtual puro [**CBaseRenderer::D oRenderSample**](cbaserenderer-dorendersample.md), que realiza el trabajo real. La clase derivada debe implementar **DoRenderSample.**

Inmediatamente antes de **llamar a DoRenderSample**, este método llama al [**método CBaseRenderer::OnRenderStart.**](cbaserenderer-onrenderstart.md) Inmediatamente después, llama al [**método CBaseRenderer::OnRenderEnd.**](cbaserenderer-onrenderend.md) La clase derivada puede invalidar esos dos métodos según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




