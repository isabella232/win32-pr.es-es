---
description: 'El método GetPreroll recupera el tiempo de prelanzamiento. Este método implementa el método IMediaSeeking:: GetPreroll.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Método CSourceSeeking. GetPreroll (Ctlutil. h)
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
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690556"
---
# <a name="csourceseekinggetpreroll-method"></a>CSourceSeeking. GetPreroll, método

El `GetPreroll` método recupera el tiempo de prelanzamiento. Este método implementa el método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

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

Puntero a una variable que recibe el tiempo de prelanzamiento. El valor se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl> | Valor de puntero **nulo**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




