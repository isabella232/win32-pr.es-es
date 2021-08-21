---
description: 'Método CBaseRenderer.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Método CBaseRenderer.BeginFlush (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70823dcc9b965aa45a7012a4c9a0210bbf77ac942d59e1ad09e028eae24a40a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158083"
---
# <a name="cbaserendererbeginflush-method"></a>Método CBaseRenderer.BeginFlush

El `BeginFlush` método comienza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El pin de entrada del filtro llama a este método cuando recibe una llamada al [**método IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) El filtro libera el subproceso de streaming y libera cualquier ejemplo que se retiene para la representación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




