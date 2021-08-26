---
description: Se llama al método OnActivate cuando se activa la página de propiedades.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Método CBasePropertyPage.OnActivate (Cprop.h)
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
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052575"
---
# <a name="cbasepropertypageonactivate-method"></a>Método CBasePropertyPage.OnActivate

Se `OnActivate` llama al método cuando se activa la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de clase base devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El [**método CBasePropertyPage::Activate**](cbasepropertypage-activate.md) llama al `OnActivate` método . En la clase derivada, invalide `OnActivate` para inicializar el cuadro de diálogo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se inicializa un control trackbar. En este ejemplo se supone **que m \_ pOwningFilter** es un puntero a una interfaz personalizada en el filtro asociado a la página de propiedades. (Use el [**método CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) para inicializar dichos punteros).


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
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




