---
description: El método IsCursorHidden recupera el estado actual del miembro de datos m \_ bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Método CBaseControlWindow.IsCursorHidden (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f7e64b056715a9f67255b6c16f62c64b65361562489ef47a37dd63548dd6e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793745"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>Método CBaseControlWindow.IsCursorHidden

El método recupera el estado actual del miembro de datos `IsCursorHidden` **m \_ bCursorHidden.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CursorHidden* 
</dt> <dd>

Puntero al valor de **m \_ bCursorHidden.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se llama sin un parámetro, devuelve OATRUE si el cursor está oculto o OAFALSE si el cursor está visible.

## <a name="remarks"></a>Comentarios

Los objetos internos deben llamar a esta función miembro sin el *parámetro CursorHidden* para evitar bloquear la sección crítica. Los objetos externos acceden a esta función miembro con el *parámetro CursorHidden* a través del método [**IVideoWindow::IsCursorHidden.**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




