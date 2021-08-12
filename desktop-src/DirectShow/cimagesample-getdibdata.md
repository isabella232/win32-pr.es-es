---
description: El método GetDIBData recupera información sobre el mapa de bits independiente del dispositivo GDI (DIB) que administra este objeto.
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
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655604"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageSample (clase)**](cimagesample.md)
</dt> </dl>

 

 




