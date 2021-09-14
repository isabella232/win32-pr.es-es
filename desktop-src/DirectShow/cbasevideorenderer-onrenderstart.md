---
description: El método OnRenderStart establece información para la representación.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Método CBaseVideoRenderer.OnRenderStart (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173805"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Método CBaseVideoRenderer.OnRenderStart

El `OnRenderStart` método establece información para la representación.

## <a name="syntax"></a>Sintaxis


```C++
void OnRenderStart(
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

Esta función miembro recupera la hora del reloj actual del sistema y la almacena en una variable miembro que se usará cuando se complete el dibujo. La función también realiza el registro de rendimiento. Se debe llamar a esta función miembro justo antes de que se inicie el dibujo.

Esta función miembro invalida [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




