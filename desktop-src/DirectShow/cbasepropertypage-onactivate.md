---
description: Se llama al método OnActivate cuando se activa la página de propiedades.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Método CBasePropertyPage. OnActivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660764"
---
# <a name="cbasepropertypageonactivate-method"></a>CBasePropertyPage. OnActivate (método)

`OnActivate`Se llama al método cuando se activa la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de la clase base devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) llama al `OnActivate` método. En la clase derivada, invalide `OnActivate` para inicializar el cuadro de diálogo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se inicializa un control TrackBar. En este ejemplo se da por supuesto que **m \_ pOwningFilter** es un puntero a una interfaz personalizada en el filtro asociado a la página de propiedades. (Use el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) para inicializar estos punteros).


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
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

 

 




