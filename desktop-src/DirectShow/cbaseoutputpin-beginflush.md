---
description: El método BeginFlush comienza una operación de vaciado. Implementa el método IPin::BeginFlush.
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Método CBaseOutputPin.BeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273175"
---
# <a name="cbaseoutputpinbeginflush-method"></a>Método CBaseOutputPin.BeginFlush

El `BeginFlush` método comienza una operación de vaciado. Implementa el [**método IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ UNEXPECTED.

## <a name="remarks"></a>Observaciones

Solo se debe llamar a este método en los pines de entrada, por lo que la implementación **de CBaseOutputPin** devuelve E \_ UNEXPECTED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




