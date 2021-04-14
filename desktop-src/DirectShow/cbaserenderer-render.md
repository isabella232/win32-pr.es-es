---
description: El método Render representa un ejemplo.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Método CBaseRenderer. Render (Renbase. h)
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
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661324"
---
# <a name="cbaserendererrender-method"></a>CBaseRenderer. Render (método)

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El filtro está detenido o *pMediaSample* es **null**.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

Este método llama al método virtual puro [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), que realiza el trabajo real. La clase derivada debe implementar **DoRenderSample**.

Inmediatamente antes de llamar a **DoRenderSample**, este método llama al método [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) . Inmediatamente después de, llama al método [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) . La clase derivada puede invalidar esos dos métodos según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




