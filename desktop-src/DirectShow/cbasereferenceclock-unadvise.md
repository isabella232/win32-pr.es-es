---
description: El método Unadvise quita una solicitud de aviso pendiente. Este método implementa el método IReferenceClock::Unadvise.
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Método CBaseReferenceClock.Unadvise (Refclock.h)
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
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652455"
---
# <a name="cbasereferenceclockunadvise-method"></a>CBaseReferenceClock.Unadvise (método)

El `Unadvise` método quita una solicitud de aviso pendiente. Este método implementa el [**método IReferenceClock::Unadvise.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise)

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

Identificador de la solicitud que se quitará. Use el valor devuelto por los métodos [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) o [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) en el parámetro *pdwAdviseToken.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Not found.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




