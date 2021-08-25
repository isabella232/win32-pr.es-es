---
description: Se produce cuando el usuario presiona y suelta una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit.KeyPress (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713100edeae3ce6b950433afb73d13f40aefb291047e98984cbd6908dde3ce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935105"
---
# <a name="inkeditkeypress-event"></a>Evento InkEdit.KeyPress

Se produce cuando el usuario presiona y suelta una tecla mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Char* 
</dt> <dd>

Entero que devuelve un código de clave ANSI numérico estándar. El *parámetro Char* se pasa por referencia; Al cambiarlo, se envía un carácter diferente al control . Al cambiar *el parámetro Char* a 0, se cancela el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyPress.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada manuscrita)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Control \[ InkEdit del evento KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**Evento KeyUp \[ InkEdit (control)\]**](inkedit-keyup.md)
</dt> </dl>

 

