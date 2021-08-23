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
ms.openlocfilehash: 94e71b3a85fdddd3ea4554575b07871ecdc09070f00c988f24f31378e9effb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640035"
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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




