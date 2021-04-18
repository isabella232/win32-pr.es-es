---
description: Se llama al método OnApplyChanges cuando el usuario aplica los cambios a la página de propiedades.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Método CBasePropertyPage. OnApplyChanges (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671613"
---
# <a name="cbasepropertypageonapplychanges-method"></a>CBasePropertyPage. OnApplyChanges, método

`OnApplyChanges`Se llama al método cuando el usuario aplica los cambios a la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de la clase base devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CBasePropertyPage:: Apply**](cbasepropertypage-apply.md) llama a `OnApplyChanges` si la marca [**\_ bDirty CBasePropertyPage:: m**](cbasepropertypage-m-bdirty.md) es **true**. Invalide `OnApplyChanges` para procesar los cambios y restablecer **m \_ bDirty** en **false**.

## <a name="examples"></a>Ejemplos


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




