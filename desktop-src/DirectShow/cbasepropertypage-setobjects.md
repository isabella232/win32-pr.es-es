---
description: El método SetObjects proporciona punteros IUnknown para los objetos asociados a la página de propiedades. Este método implementa el método IPropertyPage::SetObjects.
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage.SetObjects (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5c29d1ddc646ef05faad2bc283887265e8b85109fcb679924d9a5641ef13fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823030"
---
# <a name="cbasepropertypagesetobjects-method"></a>Método CBasePropertyPage.SetObjects

El `SetObjects` método proporciona **punteros IUnknown** para los objetos asociados a la página de propiedades. Este método implementa el **método IPropertyPage::SetObjects.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cObjects* 
</dt> <dd>

Especifica el número de punteros **IUnknown** en la matriz especificada por *ppUnk.*

</dd> <dt>

*ppUnk* 
</dt> <dd>

Especifica una matriz de **punteros IUnknown.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/>        |



 

## <a name="remarks"></a>Comentarios

Aunque *ppUnk especifica* una matriz de punteros **IUnknown,** la clase **CBasePropertyPage** está diseñada solo para admitir un objeto asociado. Si *cObjects* es mayor que 1, el método devuelve E \_ UNEXPECTED.

Si *cObjects* es igual a 1, este método llama al [**método CBasePropertyPage::OnConnect.**](cbasepropertypage-onconnect.md) Si *cObjects* es igual a 0, este método llama al [**método CBasePropertyPage::OnDisconnect.**](cbasepropertypage-ondisconnect.md) La clase derivada debe invalidar ambos métodos; Para obtener más información, vea los comentarios de esos métodos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




