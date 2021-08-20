---
description: El método GetPageInfo recupera información sobre la página de propiedades. Este método implementa el método IPropertyPage::GetPageInfo.
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Método CBasePropertyPage.GetPageInfo (Cprop.h)
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
ms.openlocfilehash: badb0678faa85b70dfa848bba7538319b905feea440339e24285f3d64b59d61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823165"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>Método CBasePropertyPage.GetPageInfo

El `GetPageInfo` método recupera información sobre la página de propiedades. Este método implementa el **método IPropertyPage::GetPageInfo.**

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

Puntero a una estructura **PROPPAGEINFO** asignada por el autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                   | Descripción                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




