---
description: 'Método CBaseDispatch.GetTypeInfoCount: el método GetTypeInfoCount recupera el número de interfaces de información de tipo que proporciona el objeto .'
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da80cdb4810ea3e598ad9483ccf52e8033ccb1a5b7ee65351e2cfcc273a3415f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660022"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>CBaseDispatch.GetTypeInfoCount (método)

El `GetTypeInfoCount` método recupera el número de interfaces de información de tipo que proporciona el objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pctinfo* 
</dt> <dd>

Puntero a una variable que recibe el número de interfaces de información de tipos proporcionadas por el objeto . Cuando el método vuelve, el valor es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseDispatch (clase)**](cbasedispatch.md)
</dt> </dl>

 

 




