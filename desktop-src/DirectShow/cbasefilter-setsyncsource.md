---
description: El método SetSyncSource establece un reloj de referencia para el filtro. Este método implementa el método IMediaFilter::SetSyncSource.
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Método CBaseFilter.SetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95e1f1b3578fa88d4616fc9e0b7d0af9fe89ab80c2e93ee32eef305b93d45478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659591"
---
# <a name="cbasefiltersetsyncsource-method"></a>Método CBaseFilter.SetSyncSource

El **método SetSyncSource** establece un reloj de referencia para el filtro. Este método implementa el [**método IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pclock* 
</dt> <dd>

Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




