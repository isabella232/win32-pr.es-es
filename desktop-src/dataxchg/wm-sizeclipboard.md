---
title: WM_SIZECLIPBOARD mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en formato CF OWNERDISPLAY y el área de cliente del visor del Portapapeles \_ ha cambiado de tamaño.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD mensaje Data Exchange
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
ms.openlocfilehash: 778caa6538992d927a0451518fcb28b82891773563614ba97c9d9df121fb69f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545324"
---
# <a name="wm_sizeclipboard-message"></a>Mensaje \_ SIZECLIPBOARD de WM

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en formato [**\_ CF OWNERDISPLAY**](standard-clipboard-formats.md) y el área de cliente del visor del Portapapeles ha cambiado de tamaño.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del Portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un objeto de memoria global que contiene una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) La estructura especifica las nuevas dimensiones del área de cliente del visor del Portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cuando la ventana del visor del Portapapeles está a punto de destruirse o cambiar de tamaño, se envía un mensaje **\_ SIZECLIPBOARD** de WM con un rectángulo nulo (0, 0, 0, 0) como nuevo tamaño. Esto permite al propietario del Portapapeles liberar sus recursos de visualización.

El propietario del Portapapeles debe usar la [**función GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear el objeto de memoria que contiene [**RECT.**](/previous-versions//dd162897(v=vs.85)) Antes de volver, el propietario del Portapapeles debe desbloquear el objeto mediante la [**función GlobalUnlock.**](/windows/desktop/api/winbase/nf-winbase-globalunlock)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

