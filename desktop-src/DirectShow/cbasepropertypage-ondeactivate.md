---
description: Se llama al método OnDeactivate cuando se destruye la ventana del cuadro de diálogo.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Método CBasePropertyPage. OnDeactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671691"
---
# <a name="cbasepropertypageondeactivate-method"></a>CBasePropertyPage. OnDeactivate (método)

`OnDeactivate`Se llama al método cuando se destruye la ventana del cuadro de diálogo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de la clase base devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CBasePropertyPage::D eactivate**](cbasepropertypage-deactivate.md) llama al `OnDeactivate` método. Invalide `OnDeactivate` para liberar los recursos que la clase derivada obtuvo en el método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , o para realizar otras tareas según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




