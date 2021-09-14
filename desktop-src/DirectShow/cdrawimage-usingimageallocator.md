---
description: El método UsingImageAllocator indica si el asignador actual es un objeto CImageAllocator.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: Método CDrawImage.UsingImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061268"
---
# <a name="cdrawimageusingimageallocator-method"></a>CDrawImage.UsingImageAllocator (método)

El `UsingImageAllocator` método indica si el asignador actual es un objeto [**CImageAllocator.**](cimageallocator.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el asignador actual es **un objeto CImageAllocator** o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




