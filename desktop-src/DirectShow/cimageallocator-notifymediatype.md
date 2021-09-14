---
description: El método NotifyMediaType informa al objeto del tipo de medio actual.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Método CImageAllocator.NotifyMediaType (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273127"
---
# <a name="cimageallocatornotifymediatype-method"></a>Método CImageAllocator.NotifyMediaType

El `NotifyMediaType` método informa al objeto del tipo de medio actual.

## <a name="syntax"></a>Sintaxis


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) o **NULL** para borrar el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método siempre que cambie el tipo de medio. Normalmente esto sucede cuando se conecta por primera vez el pin y después de un cambio de formato dinámico. El asignador usa el tipo de medio para validar las propiedades de asignador propuestas y también cuando crea ejemplos multimedia.

El **objeto CImageAllocator** almacena el *puntero pMediaType* en la variable **miembro m \_ pMediaType.** Por lo tanto, si el autor de la llamada necesita liberar el objeto **CMediaType,** debe actualizar el asignador llamando de nuevo a este método, ya sea con un nuevo puntero o con un **valor NULL.** De lo contrario, se puede producir un error cuando el asignador intenta hacer referencia al puntero anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




