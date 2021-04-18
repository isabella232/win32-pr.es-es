---
title: Mensaje de WM_PAINTCLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el \_ formato CF OWNERDISPLAY y el área cliente del visor del portapapeles debe volver a dibujarse.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Intercambio de datos de mensajes de WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665967"
---
# <a name="wm_paintclipboard-message"></a>Mensaje de PAINTCLIPBOARD de WM \_

Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y el área cliente del visor del portapapeles debe volver a dibujarse.


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un objeto de memoria global que contiene una estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) . La estructura define la parte del área de cliente que se va a pintar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Para determinar si es necesario volver a dibujar todo el área cliente o solo una parte de ella, el propietario del portapapeles debe comparar las dimensiones del área de dibujo dada en el miembro **rcPaint** de [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) con las dimensiones proporcionadas en el mensaje de [**\_ SIZECLIPBOARD de WM**](wm-sizeclipboard.md) más reciente.

El propietario del portapapeles debe utilizar la función [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear la memoria que contiene la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Antes de devolver, el propietario del portapapeles debe desbloquear esa memoria mediante la función [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SIZECLIPBOARD de WM \_**](wm-sizeclipboard.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

