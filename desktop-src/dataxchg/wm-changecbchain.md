---
title: Mensaje de WM_CHANGECBCHAIN (Winuser. h)
description: Se envía a la primera ventana de la cadena del visor del portapapeles cuando se quita una ventana de la cadena. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Intercambio de datos de mensajes de WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150422"
---
# <a name="wm_changecbchain-message"></a>Mensaje de CHANGECBCHAIN de WM \_

Se envía a la primera ventana de la cadena del visor del portapapeles cuando se quita una ventana de la cadena.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que se va a quitar de la cadena del visor del portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la siguiente ventana de la cadena que sigue a la ventana que se va a quitar. Este parámetro es **null** si la ventana que se va a quitar es la última ventana de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cada ventana del visor del portapapeles guarda el identificador en la siguiente ventana de la cadena del visor del portapapeles. Inicialmente, este identificador es el valor devuelto de la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Cuando una ventana del visor del portapapeles recibe el mensaje de **\_ CHANGECBCHAIN de WM** , debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena, a menos que la ventana siguiente sea la ventana que se va a quitar. En este caso, el visor del portapapeles debe guardar el identificador especificado por el parámetro *lParam* como la siguiente ventana de la cadena.

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

