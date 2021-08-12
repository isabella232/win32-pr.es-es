---
description: El método QueryVendorInfo recupera una cadena que contiene información del proveedor. Este método implementa el método IBaseFilter::QueryVendorInfo.
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Método CBaseFilter.QueryVendorInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff1cd8b966456df631a573ab2e8691b3be5d8bda47b21b042986204144e639b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659808"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>Método CBaseFilter.QueryVendorInfo

El `QueryVendorInfo` método recupera una cadena que contiene información del proveedor. Este método implementa el [**método IBaseFilter::QueryVendorInfo.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

Dirección de una variable que recibe un puntero a una cadena de caracteres anchos que contiene la información del proveedor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Observaciones

Para proporcionar información del proveedor para un filtro, invalide este método. Si implementa este método, use la **función CoTaskMemAlloc** para asignar memoria para la cadena. El autor de la llamada es responsable de llamar a **la función CoTaskMemFree.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




