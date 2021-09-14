---
description: El método Deactivate destruye la ventana de diálogo. Este método implementa el método IPropertyPage::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Método CBasePropertyPage.Deactivate (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062521"
---
# <a name="cbasepropertypagedeactivate-method"></a>Método CBasePropertyPage.Deactivate

El `Deactivate` método destruye la ventana de diálogo. Este método implementa el **método IPropertyPage::D eactivate.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




