---
description: Se llama al método Inactive cuando el estado se cambia a Stopped.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Método CBaseRenderer. Inactive (Renbase. h)
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
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670647"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer. Inactive (método)

`Inactive`Se llama al método cuando el estado se cambia a detenido.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El PIN de entrada llama a este método desde su propio método [**CRendererInputPin:: Inactive**](crendererinputpin-inactive.md) . El filtro llama al método [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) para liberar el ejemplo más reciente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




