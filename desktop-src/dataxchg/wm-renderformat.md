---
title: WM_RENDERFORMAT mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles si ha retrasado la representación de un formato específico del Portapapeles y si una aplicación ha solicitado datos en ese formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT mensaje Data Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884892"
---
# <a name="wm_renderformat-message"></a>Mensaje \_ RENDERFORMAT de WM

Se envía al propietario del Portapapeles si ha retrasado la representación de un formato específico del Portapapeles y si una aplicación ha solicitado datos en ese formato. El propietario del Portapapeles debe representar los datos en el formato especificado y colocarlo en el Portapapeles mediante una llamada a la [**función SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Formato [del Portapapeles](standard-clipboard-formats.md) que se va a representar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Al responder a un **mensaje \_ RENDERFORMAT de WM,** el propietario del Portapapeles no debe abrir el Portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). No es necesario abrir el Portapapeles antes de colocar los datos en respuesta a **WM \_ RENDERFORMAT** y cualquier intento de abrir el Portapapeles producirá un error porque la aplicación que solicitó que se representara el formato se mantiene abierto actualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

 





