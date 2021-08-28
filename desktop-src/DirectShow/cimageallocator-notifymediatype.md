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
ms.openlocfilehash: de8630d4189ccbbf0d90b402ebeda6b785192c098aaa1e6d29c8c2a2dac2a3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688325"
---
# <a name="cimageallocatornotifymediatype-method"></a>CImageAllocator.NotifyMediaType (método)

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

## <a name="remarks"></a>Comentarios

El filtro propietario debe llamar a este método siempre que cambie el tipo de medio. Normalmente esto sucede cuando el pin se conecta por primera vez y después de un cambio de formato dinámico. El asignador usa el tipo de medio para validar las propiedades de asignador propuestas y también cuando crea ejemplos multimedia.

El **objeto CImageAllocator** almacena el *puntero pMediaType* en la variable **miembro m \_ pMediaType.** Por lo tanto, si el autor de la llamada necesita liberar el objeto **CMediaType,** debe actualizar el asignador llamando de nuevo a este método, ya sea con un nuevo puntero o con un **valor NULL.** De lo contrario, se puede producir un error cuando el asignador intenta hacer referencia al puntero antiguo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




