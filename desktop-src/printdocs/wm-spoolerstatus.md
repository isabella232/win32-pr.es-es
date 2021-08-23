---
description: El mensaje WM SPOOLERSTATUS se envía desde el Administrador de impresión cada vez que se agrega o quita un trabajo \_ de la cola del Administrador de impresión.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2869c468517abf466b348583748e391fc1f2a4226c74b5811fffabdb5eeb89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460345"
---
# <a name="wm_spoolerstatus-message"></a>Mensaje \_ SPOOLERSTATUS de WM

El **mensaje \_ WM SPOOLERSTATUS** se envía desde el Administrador de impresión cada vez que se agrega o quita un trabajo de la cola del Administrador de impresión.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca \_ JOBSTATUS de PR.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica el número de trabajos restantes en la cola del Administrador de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Este mensaje es solo con fines informativos. Este mensaje es de aviso y no tiene semántica de entrega garantizada. Las aplicaciones no deben suponer que recibirán un mensaje \_ WM SPOOLERSTATUS para cada cambio en el estado del colador.

El mensaje \_ WM SPOOLERSTATUS no se admite después de Windows XP. Para recibir una notificación de los cambios en el estado de la cola de impresión, puede usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) y [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Impresión de mensajes de API de Spooler](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

