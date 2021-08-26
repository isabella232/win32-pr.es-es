---
description: El método GetPreroll recupera el tiempo de inscripción previa. Este método implementa el método IMediaSeeking::GetPreroll.
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Método CSourceSeeking.GetPreroll (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2d20c4487f0969a5abaf689f7c5c712e6fbb7fd83ceb7484694a3eec8599698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083965"
---
# <a name="csourceseekinggetpreroll-method"></a>CSourceSeeking.GetPreroll (método)

El `GetPreroll` método recupera el tiempo de inscripción previa. Este método implementa el [**método IMediaSeeking::GetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPreroll* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de inscripción previa. El valor se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




