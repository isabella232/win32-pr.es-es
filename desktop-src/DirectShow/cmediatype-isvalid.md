---
description: El método IsValid determina si se ha asignado un tipo principal a este objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType. IsValid (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680696"
---
# <a name="cmediatypeisvalid-method"></a>Método CMediaType. IsValid

El `IsValid` método determina si se ha asignado un tipo principal a este objeto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha asignado un tipo principal a este objeto. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

De forma predeterminada, los objetos [**CMediaType**](cmediatype.md) se inicializan con un tipo principal de GUID \_ null. Llame a este método para determinar si el objeto se ha inicializado correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




