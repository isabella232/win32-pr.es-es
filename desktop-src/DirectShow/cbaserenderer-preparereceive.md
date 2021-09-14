---
description: El método PrepareReceive prepara el filtro para representar un ejemplo.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Método CBaseRenderer.PrepareReceive (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070114"
---
# <a name="cbaserendererpreparereceive-method"></a>Método CBaseRenderer.PrepareReceive

El `PrepareReceive` método prepara el filtro para representar un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT PrepareReceive(
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



| Código devuelto                                                                                             | Descripción                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                  | Failed.<br/>                         |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | error inesperado.<br/>               |
| <dl> <dt>**EJEMPLO DE VFW \_ E \_ \_ RECHAZADO**</dt> </dl> | El filtro quita este ejemplo.<br/> |



 

## <a name="remarks"></a>Observaciones

El filtro llama a este método desde dentro del [**método CBaseRenderer::Receive,**](cbaserenderer-receive.md) antes de representar un ejemplo. Si el filtro se está ejecutando, este método programa el ejemplo para su representación.

Si el filtro ya tiene un ejemplo pendiente o si ya se ha alcanzado el final de la secuencia, el método devuelve E \_ UNEXPECTED. Posiblemente, el filtro ascendente no serializa correctamente sus llamadas de streaming.

Si el algoritmo de programación determina que se debe eliminar el ejemplo (vea [**CBaseRenderer::ScheduleSample),**](cbaserenderer-schedulesample.md)el método devuelve VFW \_ E SAMPLE \_ \_ REJECTED. Sin embargo, el método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin de entrada no pasa este código de error al filtro ascendente, porque quitar un ejemplo no es un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




