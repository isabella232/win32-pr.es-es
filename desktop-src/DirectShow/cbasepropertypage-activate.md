---
description: 'El método Activate crea la ventana de cuadro de diálogo. Este método implementa el método IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Método CBasePropertyPage. Activate (Cprop. h)
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
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670843"
---
# <a name="cbasepropertypageactivate-method"></a>CBasePropertyPage. Activate (método)

El `Activate` método crea la ventana de cuadro de diálogo. Este método implementa el método **IPropertyPage:: Activate** .

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

Puntero a una estructura **Rect** que contiene información de posición del cuadro de diálogo.

</dd> <dt>

*fModal* 
</dt> <dd>

Valor booleano que indica si el marco del cuadro de diálogo es modal (**true**) o no modal (**false**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                   | Descripción                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>       |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Error inesperado.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




