---
description: 'El método QueryFilterInfo recupera información sobre el filtro. Este método implementa el método IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter. QueryFilterInfo (Amfilter. h)
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
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661369"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>CBaseFilter. QueryFilterInfo, método

El `QueryFilterInfo` método recupera información sobre el filtro. Este método implementa el método [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .

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

Puntero a una estructura de [**\_ información de filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="remarks"></a>Observaciones

Este método copia el nombre del filtro de la variable miembro [**CBaseFilter:: m \_ pName**](cbasefilter-m-pname.md) en el miembro **achName** de la estructura de información de filtro \_ . Si **m \_ PName** es **null**, el método establece **achName** en L " \\ 0".

El método establece el miembro **pGraph** de la estructura de información de filtro \_ igual a la variable de miembro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa el recuento de referencias. El llamador debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




