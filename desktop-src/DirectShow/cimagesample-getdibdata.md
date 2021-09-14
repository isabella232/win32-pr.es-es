---
description: El método GetDIBData recupera información sobre el mapa de bits independiente del dispositivo (DIB) GDI que administra este objeto.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Método CImageSample.GetDIBData (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273084"
---
# <a name="cimagesamplegetdibdata-method"></a>Método CImageSample.GetDIBData

El método recupera información sobre el mapa de bits independiente del dispositivo `GetDIBData` (DIB) GDI que administra este objeto.

## <a name="syntax"></a>Sintaxis


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una [**estructura DIBDATA.**](dibdata.md)

## <a name="remarks"></a>Observaciones

El autor de la llamada debe **inicializar la estructura DIBDATA** antes de llamar a este método. compruebe el valor de **CImageSample::m \_ bInit**. Para inicializar la estructura, llame al [**método CImageSample::SetDIBData.**](cimagesample-setdibdata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageSample (clase)**](cimagesample.md)
</dt> </dl>

 

 




