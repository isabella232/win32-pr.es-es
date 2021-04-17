---
description: 'El método IsPageDirty indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a IPropertyPage:: Apply. Este método implementa el método IPropertyPage:: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660992"
---
# <a name="cbasepropertypageispagedirty-method"></a>CBasePropertyPage. IsPageDirty, método

El `IsPageDirty` método indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a **IPropertyPage:: Apply**. Este método implementa el método **IPropertyPage:: IsPageDirty** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) es **true** o S \_ false en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




