---
description: El método Activate crea la ventana de cuadro de diálogo. Este método implementa el método IPropertyPage::Activate.
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Método CBasePropertyPage.Activate (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108525"
---
# <a name="cbasepropertypageactivate-method"></a>Método CBasePropertyPage.Activate

El `Activate` método crea la ventana de cuadro de diálogo. Este método implementa el **método IPropertyPage::Activate.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* 
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo.

</dd> <dt>

*prect* 
</dt> <dd>

Puntero a una **estructura RECT** que contiene información de posicionamiento para el cuadro de diálogo.

</dd> <dt>

*fModal* 
</dt> <dd>

Valor booleano que indica si el marco del cuadro de diálogo es modal (**TRUE**) o modeless (**FALSE**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                   | Descripción                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Error inesperado.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




