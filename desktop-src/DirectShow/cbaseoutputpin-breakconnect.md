---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660799"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>CBaseOutputPin. BreakConnect, método

El `BreakConnect` método libera el PIN de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Desconfirma el asignador y libera las interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) y [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

Si invalida este método, llame al método de la clase base desde el método de reemplazo. De lo contrario, podría producir fugas de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




