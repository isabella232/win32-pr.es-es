---
description: Se produce cuando el usuario presiona y suelta una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716313"
---
# <a name="inkeditkeypress-event"></a>Evento InkEdit. KeyPress

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

Un entero que devuelve un valor de KeyCode ANSI estándar numérico. El parámetro *Char* se pasa por referencia; al cambiarlo, se envía un carácter diferente al control. Al cambiar el parámetro *Char* a 0 se cancela el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyPress.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Control InkEdit de evento KeyDown \[\]**](inkedit-keydown.md)
</dt> <dt>

[**Control InkEdit de evento KeyUp \[\]**](inkedit-keyup.md)
</dt> </dl>

 

