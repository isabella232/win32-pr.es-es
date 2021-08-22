---
description: El método get \_ WindowStyleEx recupera los estilos de ventana extendidos.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: CBaseControlWindow.get_WindowStyleEx método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331215"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>Método CBaseControlWindow.get \_ WindowStyleEx

El `get_WindowStyleEx` método recupera los estilos de ventana extendidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWindowStyleEx* 
</dt> <dd>

Puntero a estilos de ventana extendidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro recupera los estilos de ventana extendidos. Llama a la [**función miembro CBaseControlWindow::D oGetWindowStyle.**](cbasecontrolwindow-dogetwindowstyle.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




