---
title: WM_PAINTCLIPBOARD mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en el formato CF OWNERDISPLAY y el área de cliente del visor del Portapapeles necesita volver a \_ dibujarse.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD mensaje Datos Exchange
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
ms.openlocfilehash: 46f05aaac82bc97d4e67066f9761ac5949b4e3e97d432651ff5ddf61fea47e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914866"
---
# <a name="wm_paintclipboard-message"></a>Mensaje \_ DE WM PAINTCLIPBOARD

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y el área de cliente del visor del Portapapeles necesita volver a dibujarse.


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del Portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un objeto de memoria global que contiene una [**estructura PAINTSTRUCT.**](/windows/win32/api/winuser/ns-winuser-paintstruct) La estructura define la parte del área de cliente que se pintará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Para determinar si todo el área cliente o solo una parte de ella necesita volver a dibujarse, el propietario del Portapapeles debe comparar las dimensiones del área de dibujo dadas en el **miembro rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con las dimensiones dadas en el mensaje [**WM \_ SIZECLIPBOARD más reciente.**](wm-sizeclipboard.md)

El propietario del Portapapeles debe usar la [**función GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear la memoria que contiene la [**estructura PAINTSTRUCT.**](/windows/win32/api/winuser/ns-winuser-paintstruct) Antes de volver, el propietario del Portapapeles debe desbloquear esa memoria mediante la [**función GlobalUnlock.**](/windows/desktop/api/winbase/nf-winbase-globalunlock)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

