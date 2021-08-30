---
description: El método SetPageSite inicializa la página de propiedades y proporciona un puntero a la interfaz IPropertyPageSite del marco de propiedades. Este método implementa el método IPropertyPage::SetPageSite.
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Método CBasePropertyPage.SetPageSite (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b3a58775a984fe0d9be69d33a5eee0d0e2af1b6f1bd609f399614bf99cdc3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916365"
---
# <a name="cbasepropertypagesetpagesite-method"></a>Método CBasePropertyPage.SetPageSite

El método inicializa la página de propiedades y proporciona un puntero a la interfaz `SetPageSite` **IPropertyPageSite** del marco de propiedades. Este método implementa el **método IPropertyPage::SetPageSite.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPageSite* 
</dt> <dd>

Puntero a la **interfaz IPropertyPageSite.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="remarks"></a>Comentarios

El método almacena el *puntero pPageSite* en la variable miembro [**CBasePropertyPage::m \_ pPageSite.**](cbasepropertypage-m-ppagesite.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




