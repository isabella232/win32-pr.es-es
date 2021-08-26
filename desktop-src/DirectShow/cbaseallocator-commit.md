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
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087585"
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



 

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, llame [**al método CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) para especificar los requisitos del búfer.

Este método llama al método virtual [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) para asignar la memoria para los búferes. Las clases derivadas pueden invalidar **Alloc**. Si una operación de desaprobación está pendiente, se cancela.

Debe llamar a este método antes de llamar [**al método CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




