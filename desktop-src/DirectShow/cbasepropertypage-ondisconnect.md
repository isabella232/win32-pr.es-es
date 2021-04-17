---
description: Se llama al método OnDisconnect cuando la página de propiedades debe liberar el objeto asociado.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Método CBasePropertyPage. OnDisconnection (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670510"
---
# <a name="cbasepropertypageondisconnect-method"></a>CBasePropertyPage. OnDisconnection (método)

`OnDisconnect`Se llama al método cuando la página de propiedades debe liberar el objeto asociado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de la clase base devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) llama al `OnDisconnect` método. Invalide `OnDisconnect` para liberar los punteros que se obtuvieron en el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) .

## <a name="examples"></a>Ejemplos


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
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

 

 




