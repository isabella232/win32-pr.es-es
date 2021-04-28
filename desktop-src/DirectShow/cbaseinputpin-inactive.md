---
description: 'Método CBaseInputPin.Inactive: el método inactivo notifica al pin que el filtro ya no está activo.'
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Método CBaseInputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1324e9e2641e5e05bc3b0429ee269098c13d4bae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099733"
---
# <a name="cbaseinputpininactive-method"></a>CBaseInputPin.Inactive (método)

El `Inactive` método notifica al pin que el filtro ya no está activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                          | Descripción                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Correcto.<br/>                          |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | No hay ningún asignador de memoria disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::Inactive.**](cbasepin-inactive.md) Llama al [**método IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desasignar el asignador de memoria.

Si invalida este método, llame al método de clase base desde el método de reemplazo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




