---
description: 'El método SetObjects proporciona punteros IUnknown para los objetos asociados a la página de propiedades. Este método implementa el método IPropertyPage:: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage. SetObjects (Cprop. h)
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
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671269"
---
# <a name="cbasepropertypagesetobjects-method"></a>CBasePropertyPage. SetObjects, método

El `SetObjects` método proporciona punteros **IUnknown** para los objetos asociados a la página de propiedades. Este método implementa el método **IPropertyPage:: SetObjects** .

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

Especifica el número de punteros **IUnknown** en la matriz especificada por *ppUnk*.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Especifica una matriz de punteros **IUnknown** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/>        |



 

## <a name="remarks"></a>Observaciones

Aunque *ppUnk* especifica una matriz de punteros **IUnknown** , la clase **CBasePropertyPage** está diseñada únicamente para admitir un objeto asociado. Si *cObjects* es mayor que 1, el método devuelve E \_ inesperado.

Si *cObjects* es igual a 1, este método llama al método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) . Si *cObjects* es igual a 0, este método llama al método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) . La clase derivada debe reemplazar ambos métodos; para obtener más información, vea los comentarios de estos métodos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




