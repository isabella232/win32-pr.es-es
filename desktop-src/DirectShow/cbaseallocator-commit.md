---
description: 'El método commit asigna la memoria de los búferes. Este método implementa el método IMemAllocator:: commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Método CBaseAllocator. Commit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670880"
---
# <a name="cbaseallocatorcommit-method"></a>CBaseAllocator. Commit (método)

El `Commit` método asigna la memoria de los búferes. Este método implementa el método [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la lista siguiente.



| Código devuelto                                                                                       | Descripción                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se especificaron los requisitos de búfer.<br/> |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame al método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) para especificar los requisitos de búfer.

Este método llama al método virtual [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) para asignar la memoria de los búferes. Las clases derivadas pueden invalidar **Alloc**. Si hay pendiente una operación de desconfirmación, se cancela.

Debe llamar a este método antes de llamar al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




