---
description: El método get \_ Visible recupera la visibilidad de la ventana actual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: CBaseControlWindow.get_Visible método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974019"
---
# <a name="cbasecontrolwindowget_visible-method"></a>Método CBaseControlWindow.get \_ Visible

El `get_Visible` método recupera la visibilidad de la ventana actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVisible* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 está desactivado, 1 está on).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve 1 si la ventana tiene el estilo VISIBLE de \_ WS; 0 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




