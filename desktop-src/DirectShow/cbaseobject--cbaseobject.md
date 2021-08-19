---
description: 'Destructor CBaseObject.~CBaseObject: método destructor.'
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: Destructor CBaseObject.~CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6508591f30a14e345cb67f9fe3a098dbaf357b6f60f57232af9f7af4570b6f6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640185"
---
# <a name="cbaseobjectcbaseobject-destructor"></a>Destructor CBaseObject.~CBaseObject

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CBaseObject();
```



## <a name="remarks"></a>Comentarios

Este método disminuye el recuento de objetos activos. (Vea [**CBaseObject::ObjectsActive).**](cbaseobject-objectsactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseObject (clase)**](cbaseobject.md)
</dt> </dl>

 

 




