---
description: 'El método move coloca y cambia el tamaño del cuadro de diálogo. Este método implementa el método IPropertyPage:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Método CBasePropertyPage. Move (Cprop. h)
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
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671090"
---
# <a name="cbasepropertypagemove-method"></a>CBasePropertyPage. Move (método)

El `Move` método coloca y cambia el tamaño del cuadro de diálogo. Este método implementa el método **IPropertyPage:: Move** .

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

Puntero a una estructura **Rect** que contiene la información de posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




