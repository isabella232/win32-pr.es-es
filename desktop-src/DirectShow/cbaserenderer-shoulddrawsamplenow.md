---
description: El método ShouldDrawSampleNow determina cómo se programa una muestra para su representación.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Método CBaseRenderer.ShouldDrawSampleNow (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061766"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>Método CBaseRenderer.ShouldDrawSampleNow

El `ShouldDrawSampleNow` método determina cómo se programa una muestra para su representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio del ejemplo.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a una variable que contiene la hora de finalización del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ FALSE. Si la clase derivada invalida este método, devuelva uno de los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El ejemplo debe representarse inmediatamente.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El ejemplo debe programarse para su representación, en función de las marcas de tiempo.<br/> |
| <dl> <dt>**Código de error**</dt> </dl> | No represente este ejemplo.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

El [**método CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) llama a este método. De forma predeterminada, los ejemplos siempre se programan para su representación en función de sus marcas de tiempo. La clase derivada puede invalidar este método; por ejemplo, para implementar el control de calidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




