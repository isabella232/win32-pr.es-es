---
description: El método ReallocFormatBuffer reasigna el bloque de formato a un nuevo tamaño.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType. ReallocFormatBuffer (mtype. h)
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
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670559"
---
# <a name="cmediatypereallocformatbuffer-method"></a>CMediaType. ReallocFormatBuffer, método

El `ReallocFormatBuffer` método reasigna el bloque de formato a un nuevo tamaño.

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

Devuelve un puntero al nuevo bloque si se realiza correctamente. De lo contrario, devuelve un puntero al bloque de formato antiguo o **null**.

## <a name="remarks"></a>Observaciones

Este método asigna un nuevo bloque de formato. Copia tanto como sea posible el bloque de formato existente en el nuevo bloque de formato. Si el nuevo bloque es más pequeño que el bloque existente, el bloque de formato existente se trunca. Si el nuevo bloque es mayor, el contenido del espacio adicional no está definido. No se establecen explícitamente en cero.

El método actualiza los miembros **cbFormat** y **pbFormat** de la estructura de **\_ \_ tipo de medio am** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




