---
title: Mensaje de WM_SIZECLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el \_ formato CF OWNERDISPLAY y el área cliente del visor del portapapeles ha cambiado de tamaño.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Intercambio de datos de mensajes de WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802546"
---
# <a name="wm_sizeclipboard-message"></a>Mensaje de SIZECLIPBOARD de WM \_

Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y el área cliente del visor del portapapeles ha cambiado de tamaño.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un objeto de memoria global que contiene una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . La estructura especifica las nuevas dimensiones del área cliente del visor del portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cuando se va a destruir o cambiar el tamaño de la ventana del visor del portapapeles, se envía un mensaje de **WM \_ SIZECLIPBOARD** con un rectángulo nulo (0, 0, 0,0) como el nuevo tamaño. Esto permite que el propietario del portapapeles libere sus recursos para mostrar.

El propietario del portapapeles debe utilizar la función [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear el objeto de memoria que contiene [**Rect**](/previous-versions//dd162897(v=vs.85)). Antes de devolver, el propietario del portapapeles debe desbloquear el objeto mediante la función [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

