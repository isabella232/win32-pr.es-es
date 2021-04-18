---
description: 'El método Apply aplica los valores de la página de propiedades actual al objeto asociado a la página de propiedades. Este método implementa el método IPropertyPage:: Apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage. Apply (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660768"
---
# <a name="cbasepropertypageapply-method"></a>CBasePropertyPage. Apply (método)

El `Apply` método aplica los valores actuales de la página de propiedades al objeto asociado a la página de propiedades. Este método implementa el método **IPropertyPage:: Apply** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="remarks"></a>Observaciones

Si la marca [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) es **true**, este método llama al método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) . Invalide **OnApplyChanges** para aplicar los cambios al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




