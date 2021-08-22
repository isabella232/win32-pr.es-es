---
description: El método Active crea un subproceso de trabajo que extrae datos del pin de salida. Este método también confirma el asignador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin.Active (Pullpin.h)
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
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073529"
---
# <a name="cpullpinactive-method"></a>Método CPullPin.Active

El **método Active** crea un subproceso de trabajo que extrae datos del pin de salida. Este método también confirma el asignador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | La conexión de pin no se estableció correctamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | No se pudo crear el subproceso o el subproceso ya existe.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método cuando el filtro propietario se active. (Si el pin de entrada deriva de [**CBasePin,**](cbasepin.md)invalide el [**método CBasePin::Active).**](cbasepin-active.md)

Antes de llamar a este método, llame [**al método CPullPin::Conectar**](cpullpin-connect.md) para establecer la conexión con el pin de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




