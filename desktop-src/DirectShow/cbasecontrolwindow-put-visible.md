---
description: El método put \_ Visible muestra u oculta la ventana.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: CBaseControlWindow.put_Visible método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246860"
---
# <a name="cbasecontrolwindowput_visible-method"></a>CBaseControlWindow.put \_ (método Visible)

El `put_Visible` método muestra u oculta la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Visible* 
</dt> <dd>

Marca booleana de Automation (0 significa que la ventana está oculta, 1 significa que se muestra la ventana).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




