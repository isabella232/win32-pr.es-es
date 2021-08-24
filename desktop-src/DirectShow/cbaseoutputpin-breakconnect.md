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
ms.openlocfilehash: 9ae03edb843a2b9c6f1cbc98a46c2464de0e76e2eecf5d77bc309efa2dd60fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793225"
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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




