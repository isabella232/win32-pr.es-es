---
description: El método Deactivate destruye la ventana del cuadro de diálogo. Este método implementa el método IPropertyPage::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Método CBasePropertyPage. Deactivate (Cprop. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660767"
---
# <a name="cbasepropertypagedeactivate-method"></a>CBasePropertyPage. Deactivate (método)

El `Deactivate` método destruye la ventana del cuadro de diálogo. Este método implementa el método **IPropertyPage::D eactivate** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




