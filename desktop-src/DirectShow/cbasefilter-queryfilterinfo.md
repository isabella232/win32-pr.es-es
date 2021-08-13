---
description: El método QueryFilterInfo recupera información sobre el filtro. Este método implementa el método IBaseFilter::QueryFilterInfo.
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter.QueryFilterInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341745"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Método CBaseFilter.QueryFilterInfo

El `QueryFilterInfo` método recupera información sobre el filtro. Este método implementa el método [**IBaseFilter::QueryFilterInfo.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntero a una [**estructura FILTER \_ INFO.**](/windows/win32/api/strmif/ns-strmif-filter_info)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Comentarios

Este método copia el nombre del filtro de la variable miembro [**CBaseFilter::m \_ pName**](cbasefilter-m-pname.md) en el **miembro achName** de la estructura FILTER \_ INFO. Si **m \_ pName** es **NULL,** el método establece **achName** en L' \\ 0'.

El método establece el **miembro pGraph** de la estructura FILTER INFO igual a la variable miembro \_ [**CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa el recuento de referencias. El autor de la llamada debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




