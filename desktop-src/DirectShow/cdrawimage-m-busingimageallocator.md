---
description: La \_ variable miembro m bUsingImageAllocator indica si el asignador de la conexión de PIN es un objeto CImageAllocator. Si el valor es TRUE, el asignador es un objeto CImageAllocator (o se deriva de esa clase).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Miembro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
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
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671316"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Miembro bUsingImageAllocator CDrawImage:: m \_

La `m_bUsingImageAllocator` variable miembro indica si el asignador de la conexión de PIN es un objeto **CImageAllocator** . Si el valor es **true**, el asignador es un objeto **CImageAllocator** (o se deriva de esa clase).

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Observaciones

Cuando el valor es **true**, el objeto **CDrawImage** puede usar las funciones **bitblt** y **StretchBlt** de GDI para representar la imagen, en lugar de las funciones **SetDIBitsToDevice** y **StretchDIBits** más lentas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




