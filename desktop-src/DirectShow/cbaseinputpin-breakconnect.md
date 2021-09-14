---
description: 'Método CBaseInputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173834"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Método CBaseInputPin.BreakConnect

El `BreakConnect` método libera el pin de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Desasigna el asignador y libera la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Si invalida este método, llame al método de clase base desde el método de reemplazo. De lo contrario, podría provocar pérdidas de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




