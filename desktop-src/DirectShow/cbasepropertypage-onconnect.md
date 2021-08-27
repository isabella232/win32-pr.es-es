---
description: El método OnConnect proporciona un puntero IUnknown al objeto asociado a la página de propiedades.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Método CBasePropertyPage.OnConnect (Cprop.h)
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
ms.openlocfilehash: edc5448a20320e9bf74da7511bf6ae9fb9d95facc9b7973bbcd688127b495fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056105"
---
# <a name="cbasepropertypageonconnect-method"></a>Método CBasePropertyPage.OnConnect

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

Puntero a **la interfaz IUnknown** del objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La implementación de clase base devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El [**método CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) llama al `OnConnect` método . Invalide este método para almacenar un puntero al objeto especificado por *pUnknown*. Puede almacenar el propio *puntero pUnknown* o consultar ese puntero para otras interfaces. Si almacena el puntero *pUnknown,* llame a **AddRef antes** de que `OnConnect` se devuelva.

En el [**método CBasePropertyPage::OnActivate,**](cbasepropertypage-onactivate.md) use el puntero almacenado (o punteros) para recuperar los valores iniciales de las propiedades del cuadro de diálogo. En el [**método CBasePropertyPage::OnApplyChanges,**](cbasepropertypage-onapplychanges.md) vuelva a aplicar los cambios al objeto . Libere todos los punteros del [**método CBasePropertyPage::OnDisconnect.**](cbasepropertypage-ondisconnect.md)

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
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




