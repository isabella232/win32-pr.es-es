---
description: Se llama al método OnApplyChanges cuando el usuario aplica cambios a la página de propiedades.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Método CBasePropertyPage.OnApplyChanges (Cprop.h)
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
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823111"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Método CBasePropertyPage.OnApplyChanges

Se `OnApplyChanges` llama al método cuando el usuario aplica cambios a la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La implementación de clase base devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El [**método CBasePropertyPage::Apply**](cbasepropertypage-apply.md) llama a si la marca `OnApplyChanges` [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) es **TRUE.** Invalide `OnApplyChanges` para procesar los cambios y **\_ restablezca m bDirty** en **FALSE.**

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
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




