---
description: 'Método CBaseOutputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: 746783a73892bc34273da4b020446f2668a19cd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096223"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Método CBaseOutputPin.BreakConnect

El `BreakConnect` método libera el pin de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Desasigna el asignador y libera las interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) [**e IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

Si invalida este método, llame al método de clase base desde el método de reemplazo. De lo contrario, podría provocar pérdidas de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




