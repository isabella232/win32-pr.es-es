---
description: 'Método CBaseOutputPin.EndFlush: el método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin::EndFlush.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Método CBaseOutputPin.EndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a85df585a570d7b35a0ac052c922b23dcb605cf4869b3a44cab880f9b6bef21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910485"
---
# <a name="cbaseoutputpinendflush-method"></a>Método CBaseOutputPin.EndFlush

El `EndFlush` método finaliza una operación de vaciado. Este método implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ UNEXPECTED.

## <a name="remarks"></a>Comentarios

Solo se debe llamar a este método en los pines de entrada, por lo que la implementación **de CBaseOutputPin** devuelve E \_ UNEXPECTED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




