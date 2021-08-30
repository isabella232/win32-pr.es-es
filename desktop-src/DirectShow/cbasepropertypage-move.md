---
description: El método Move coloca y cambia el tamaño del cuadro de diálogo. Este método implementa el método IPropertyPage::Move.
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Método CBasePropertyPage.Move (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 274295c08895fe28b0f3abe3438496719f7fcdfa2dae486401de6babb624cc31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052555"
---
# <a name="cbasepropertypagemove-method"></a>CBasePropertyPage.Move (método)

El `Move` método coloca y cambia el tamaño del cuadro de diálogo. Este método implementa el **método IPropertyPage::Move.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prect* 
</dt> <dd>

Puntero a una **estructura RECT** que contiene la información de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




