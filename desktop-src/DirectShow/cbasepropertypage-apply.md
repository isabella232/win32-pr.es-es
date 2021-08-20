---
description: El método Apply aplica los valores de página de propiedades actuales al objeto asociado a la página de propiedades. Este método implementa el método IPropertyPage::Apply.
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage.Apply (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9350aa7aaa4e2bfdcb72385d26b09b9d7a9bdf33deb05e273b0663485da1a5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823248"
---
# <a name="cbasepropertypageapply-method"></a>CBasePropertyPage.Apply (método)

El `Apply` método aplica los valores de página de propiedades actuales al objeto asociado a la página de propiedades. Este método implementa el **método IPropertyPage::Apply.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/> |



 

## <a name="remarks"></a>Comentarios

Si la [**marca CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) es **TRUE,** este método llama al método [**CBasePropertyPage::OnApplyChanges.**](cbasepropertypage-onapplychanges.md) Invalide **OnApplyChanges** para aplicar los cambios al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




