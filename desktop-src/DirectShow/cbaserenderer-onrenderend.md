---
description: Se llama al método OnRenderEnd después de representar un ejemplo.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Método CBaseRenderer.OnRenderEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fe720ecaa6cc72a0efae3fceda3bb307573077caee6de5ac4309207883c994d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526545"
---
# <a name="cbaserendereronrenderend-method"></a>Método CBaseRenderer.OnRenderEnd

Se `OnRenderEnd` llama al método después de representar un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnRenderEnd(
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

El [**método CBaseRenderer::Render**](cbaserenderer-render.md) llama a este método. No hace nada en la clase base, pero la clase derivada puede invalidarla. por ejemplo, para recopilar datos de control de calidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




