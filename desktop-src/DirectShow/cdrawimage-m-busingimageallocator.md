---
description: La variable miembro m bUsingImageAllocator indica si el asignador de la conexión de pin \_ es un objeto CImageAllocator. Si el valor es TRUE, el asignador es un objeto CImageAllocator (o se deriva de esa clase).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: CDrawImage::m_bUsingImageAllocator miembro (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657142"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Miembro CDrawImage::m \_ bUsingImageAllocator

La `m_bUsingImageAllocator` variable miembro indica si el asignador de la conexión de pin es un objeto **CImageAllocator.** Si el valor es **TRUE,** el asignador es un **objeto CImageAllocator** (o se deriva de esa clase).

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Observaciones

Cuando el valor es **TRUE,** el objeto **CDrawImage** puede usar las funciones **BitBlt** y **StretchBlt** de GDI para representar la imagen, en lugar de las funciones **SetDIBitsToDevice** y **StretchDIBits más lentas.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




