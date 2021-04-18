---
description: 'El método SetPageSite inicializa la página de propiedades y proporciona un puntero a la interfaz IPropertyPageSite del marco de propiedad. Este método implementa el método IPropertyPage:: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Método CBasePropertyPage. SetPageSite (Cprop. h)
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
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660248"
---
# <a name="cbasepropertypagesetpagesite-method"></a>CBasePropertyPage. SetPageSite, método

El `SetPageSite` método inicializa la página de propiedades y proporciona un puntero a la interfaz **IPropertyPageSite** del marco de propiedad. Este método implementa el método **IPropertyPage:: SetPageSite** .

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

Puntero a la interfaz **IPropertyPageSite** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="remarks"></a>Observaciones

El método almacena el puntero *pPageSite* en la variable miembro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




