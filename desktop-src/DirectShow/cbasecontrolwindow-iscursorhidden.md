---
description: El método IsCursorHidden recupera el estado actual del \_ miembro de datos m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Método CBaseControlWindow. IsCursorHidden (Ctlutil. h)
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
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661387"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>CBaseControlWindow. IsCursorHidden, método

El `IsCursorHidden` método recupera el estado actual del miembro de datos **m \_ bCursorHidden** .

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

Puntero al valor de **m \_ bCursorHidden**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se llama sin un parámetro, devuelve OATRUE si el cursor está oculto, o OAFALSE si el cursor está visible.

## <a name="remarks"></a>Observaciones

Los objetos internos deben llamar a esta función miembro sin el parámetro *CursorHidden* para evitar el bloqueo de la sección crítica. Los objetos externos acceden a esta función miembro con el parámetro *CursorHidden* a través del método [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




