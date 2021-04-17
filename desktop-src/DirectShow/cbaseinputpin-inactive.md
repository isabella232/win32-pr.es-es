---
description: El método Inactive notifica al pin que el filtro ya no está activo.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Método CBaseInputPin. Inactive (Amfilter. h)
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
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660342"
---
# <a name="cbaseinputpininactive-method"></a>CBaseInputPin. Inactive (método)

El `Inactive` método notifica al pin que el filtro ya no está activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                          | Descripción                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                 | Correcto.<br/>                          |
| <dl> <dt>**VFW \_ E \_ no \_ asignador**</dt> </dl> | No hay ningún asignador de memoria disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBasePin:: Inactive**](cbasepin-inactive.md) . Llama al método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desasignar el asignador de memoria.

Si invalida este método, llame al método de la clase base desde el método de reemplazo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




