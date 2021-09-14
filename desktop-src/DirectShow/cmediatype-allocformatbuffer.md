---
description: El método AllocFormatBuffer asigna memoria para el bloque de formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Método CMediaType.AllocFormatBuffer (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246849"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Método CMediaType.AllocFormatBuffer

El `AllocFormatBuffer` método asigna memoria para el bloque de formato.

## <a name="syntax"></a>Sintaxis


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*length* 
</dt> <dd>

Tamaño necesario para el bloque de formato, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al nuevo bloque si se realiza correctamente. De lo contrario, devuelve **NULL.**

## <a name="remarks"></a>Observaciones

Si el método asigna correctamente un nuevo bloque de formato, libera el bloque de formato existente. Si se produce un error en la asignación, el método deja el bloque de formato existente.

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

 

 




