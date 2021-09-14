---
description: El método Commit asigna la memoria para los búferes. Este método implementa el método IMemAllocator::Commit.
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Método CBaseAllocator.Commit (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361427"
---
# <a name="cbaseallocatorcommit-method"></a>Método CBaseAllocator.Commit

El `Commit` método asigna la memoria para los búferes. Este método implementa el [**método IMemAllocator::Commit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la lista siguiente.



| Código devuelto                                                                                       | Descripción                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se especificaron los requisitos de búfer.<br/> |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame [**al método CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) para especificar los requisitos del búfer.

Este método llama al método virtual [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) para asignar la memoria para los búferes. Las clases derivadas pueden invalidar **Alloc**. Si hay una operación de desaprobación pendiente, se cancela.

Debe llamar a este método antes de llamar al [**método CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




