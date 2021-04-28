---
description: 'Método CBaseOutputPin.Active: el método Active notifica al pin que el filtro ahora está activo.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Método CBaseOutputPin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096213"
---
# <a name="cbaseoutputpinactive-method"></a>Método CBaseOutputPin.Active

El `Active` método notifica al pin que el filtro ahora está activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                          | Descripción                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Correcto.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | No hay ningún asignador disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::Active.**](cbasepin-active.md) Llama al método [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) en el asignador para asignar memoria para los búferes.

Si invalida este método, llame al método de clase base desde el método de reemplazo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




