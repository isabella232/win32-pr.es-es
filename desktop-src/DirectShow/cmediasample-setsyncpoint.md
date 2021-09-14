---
description: El método SetSyncPoint especifica si el principio de este ejemplo es un punto de sincronización. Este método implementa el método IMediaSample::SetSyncPoint.
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Método CMediaSample.SetSyncPoint (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251133"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Método CMediaSample.SetSyncPoint

El `SetSyncPoint` método especifica si el principio de este ejemplo es un punto de sincronización. Este método implementa el [**método IMediaSample::SetSyncPoint.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

Valor booleano que especifica si se trata de un punto de sincronización. Si **es TRUE,** se trata de un punto de sincronización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método actualiza la variable [**miembro CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica la propiedad synchronization-point.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




