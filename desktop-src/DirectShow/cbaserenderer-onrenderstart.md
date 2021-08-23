---
description: Se llama al método OnRenderStart cuando la representación está a punto de iniciarse.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Método CBaseRenderer.OnRenderStart (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626dc1dbcb82aeec94ebe514e686d197cb17bbdd7807ac38057412617182bf55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157659"
---
# <a name="cbaserendereronrenderstart-method"></a>Método CBaseRenderer.OnRenderStart

Se `OnRenderStart` llama al método cuando la representación está a punto de iniciarse.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnRenderStart(
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

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [**método CBaseRenderer::Render**](cbaserenderer-render.md) llama a este método. No hace nada en la clase base, pero la clase derivada puede invalidarla; por ejemplo, para recopilar datos de control de calidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




