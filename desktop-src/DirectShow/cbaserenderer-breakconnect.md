---
description: El método BreakConnect libera el PIN de entrada de una conexión.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671080"
---
# <a name="cbaserendererbreakconnect-method"></a>CBaseRenderer. BreakConnect, método

El `BreakConnect` método libera el PIN de entrada de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                         | Descripción                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | El PIN no estaba conectado.<br/>  |
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Correcto.<br/>                    |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl> | El filtro todavía está activo.<br/> |



 

## <a name="remarks"></a>Observaciones

El PIN de entrada del filtro llama a este método desde dentro de su propio `BreakConnect` método. (Para obtener más información, vea [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md)). El filtro realiza una contabilidad interna, como el restablecimiento de la marca de fin de secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




