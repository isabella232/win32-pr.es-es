---
title: Mensaje de WM_RENDERFORMAT (Winuser. h)
description: Se envía al propietario del portapapeles si ha retrasado la representación de un formato específico del portapapeles y si una aplicación ha solicitado datos en ese formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Intercambio de datos de mensajes de WM_RENDERFORMAT
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359740"
---
# <a name="wm_renderformat-message"></a>Mensaje de RENDERFORMAT de WM \_

Se envía al propietario del portapapeles si ha retrasado la representación de un formato específico del portapapeles y si una aplicación ha solicitado datos en ese formato. El propietario del portapapeles debe representar los datos en el formato especificado y colocarlos en el portapapeles mediante una llamada a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[Formato del portapapeles](standard-clipboard-formats.md) que se va a representar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cuando se responde a un mensaje de **\_ RENDERFORMAT de WM** , el propietario del portapapeles no debe abrir el portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). No es necesario abrir el portapapeles antes de colocar los datos en respuesta a **WM \_ RENDERFORMAT** y se producirá un error al intentar abrir el portapapeles, ya que la aplicación que solicitó el formato para representarlo tiene abierto el portapapeles.

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

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**RENDERALLFORMATS de WM \_**](wm-renderallformats.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

 





