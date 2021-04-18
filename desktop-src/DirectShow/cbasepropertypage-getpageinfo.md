---
description: 'El método GetPageInfo recupera información sobre la página de propiedades. Este método implementa el método IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Método CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671323"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>CBasePropertyPage. GetPageInfo (método)

El `GetPageInfo` método recupera información sobre la página de propiedades. Este método implementa el método **IPropertyPage:: GetPageInfo** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Puntero a una estructura **PROPPAGEINFO** asignada por el llamador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                   | Descripción                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




