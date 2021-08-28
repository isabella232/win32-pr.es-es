---
description: El método IsPageDirty indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a IPropertyPage::Apply. Este método implementa el método IPropertyPage::IsPageDirty.
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage.IsPageDirty (Cprop.h)
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
ms.openlocfilehash: 72b818ce117990f6f91ee58b8605e9d8cff9734fa9114d7f6114ed11d53a9521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108505"
---
# <a name="cbasepropertypageispagedirty-method"></a>Método CBasePropertyPage.IsPageDirty

El método indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a `IsPageDirty` **IPropertyPage::Apply**. Este método implementa el **método IPropertyPage::IsPageDirty.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) es **TRUE** o S FALSE en caso \_ contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




