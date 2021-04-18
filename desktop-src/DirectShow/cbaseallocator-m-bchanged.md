---
description: Marca que indica si los requisitos de búfer han cambiado.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Miembro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671449"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Miembro bChanged CBaseAllocator:: m \_

Marca que indica si los requisitos de búfer han cambiado. El método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) establece el valor en **true**. En una clase derivada, el método virtual puro [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) debe volver a establecer el valor en **false**. Una vez que se han asignado los búferes, no es necesario volver a asignarlos, mientras que *m \_ BChanged* es **false**.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




