---
description: El método ReallocFormatBuffer reasigna el bloque de formato a un nuevo tamaño.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType.ReallocFormatBuffer (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bd4d7bd27c3698f1e30c690f755f445ffaffeff37c88f27d0a5c8ba58cd2d32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768175"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Método CMediaType.ReallocFormatBuffer

El `ReallocFormatBuffer` método reallocate el bloque de formato a un nuevo tamaño.

## <a name="syntax"></a>Sintaxis


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*length* 
</dt> <dd>

Nuevo tamaño necesario para el bloque de formato, en bytes. Debe ser mayor que cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al nuevo bloque si se realiza correctamente. De lo contrario, devuelve un puntero al bloque de formato antiguo o **NULL.**

## <a name="remarks"></a>Comentarios

Este método asigna un nuevo bloque de formato. Copia tanto como sea posible del bloque de formato existente en el nuevo bloque de formato. Si el nuevo bloque es menor que el bloque existente, se trunca el bloque de formato existente. Si el nuevo bloque es mayor, el contenido del espacio adicional no está definido. No se establecen explícitamente en cero.

El método actualiza los **miembros cbFormat** y **pbFormat** de la **estructura AM MEDIA \_ \_ TYPE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




