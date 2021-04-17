---
description: El método alconnect proporciona un puntero IUnknown al objeto asociado a la página de propiedades.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Método CBasePropertyPage. alconnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661240"
---
# <a name="cbasepropertypageonconnect-method"></a>CBasePropertyPage. alconnect (método)

El `OnConnect` método proporciona un puntero **IUnknown** al objeto asociado a la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnknown* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La implementación de la clase base devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) llama al `OnConnect` método. Invalide este método para almacenar un puntero al objeto especificado por *pUnknown*. Puede almacenar el puntero *pUnknown* en sí o consultar ese puntero para otras interfaces. Si almacena el puntero *pUnknown* , llame a **AddRef** antes de que `OnConnect` devuelva.

En el método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , use el puntero almacenado (o los punteros) para recuperar los valores iniciales de las propiedades del cuadro de diálogo. En el método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , aplique los cambios de nuevo al objeto. Libera todos los punteros en el método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) .

## <a name="examples"></a>Ejemplos


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




