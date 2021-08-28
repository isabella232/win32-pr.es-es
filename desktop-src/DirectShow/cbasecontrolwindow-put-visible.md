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
ms.openlocfilehash: f2c8565d14c58d520a91c682e55d3dbc2ba079cf956213bdc61d044834d690c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793296"
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

 

 




