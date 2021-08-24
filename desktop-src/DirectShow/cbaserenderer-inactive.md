---
description: Se llama al método Inactivo cuando el estado cambia a detenido.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Método CBaseRenderer.Inactive (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652405"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer.Inactive (método)

Se `Inactive` llama al método cuando se cambia el estado a detenido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El pin de entrada llama a este método desde su propio [**método CRendererInputPin::Inactive.**](crendererinputpin-inactive.md) El filtro llama al [**método CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) para liberar el ejemplo más reciente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




