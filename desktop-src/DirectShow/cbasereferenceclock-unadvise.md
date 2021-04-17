---
description: 'El método Unadvise quita una solicitud de notificación pendiente. Este método implementa el método IReferenceClock:: unvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Método CBaseReferenceClock. unvise (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661185"
---
# <a name="cbasereferenceclockunadvise-method"></a>CBaseReferenceClock. Unadvise (método)

El `Unadvise` método quita una solicitud de notificación pendiente. Este método implementa el método [**IReferenceClock:: unvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

Identificador de la solicitud que se va a quitar. Use el valor devuelto por los métodos [**CBaseReferenceClock:: AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) en el parámetro *pdwAdviseToken* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Not found.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




