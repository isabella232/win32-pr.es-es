---
description: El método activo crea un subproceso de trabajo que extrae datos del PIN de salida. Este método también confirma el asignador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671823"
---
# <a name="cpullpinactive-method"></a>CPullPin. Active (método)

El método **activo** crea un subproceso de trabajo que extrae datos del PIN de salida. Este método también confirma el asignador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                                   |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | La conexión del PIN no se estableció correctamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | No se pudo crear el subproceso o el subproceso ya existe.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método cuando el filtro propietario se active. (Si el PIN de entrada se deriva de [**CBasePin**](cbasepin.md), invalide el método [**CBasePin:: Active**](cbasepin-active.md) ).

Antes de llamar a este método, llame al método [**CPullPin:: Connect**](cpullpin-connect.md) para establecer la conexión con el PIN de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




