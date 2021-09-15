---
description: El mensaje WM SPOOLERSTATUS se envía desde el Administrador de impresión cada vez que se agrega o quita un trabajo \_ de la cola del Administrador de impresión.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570540"
---
# <a name="wm_spoolerstatus-message"></a>Mensaje \_ DE WM SPOOLERSTATUS

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

Marca \_ JOBSTATUS de pr.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica el número de trabajos restantes en la cola del Administrador de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje es solo con fines informativos. Este mensaje es de aviso y no tiene semántica de entrega garantizada. Las aplicaciones no deben asumir que recibirán un mensaje \_ WM SPOOLERSTATUS para cada cambio en el estado del colador.

El mensaje \_ WM SPOOLERSTATUS no se admite después Windows XP. Para recibir notificaciones de los cambios en el estado de la cola de impresión, puede usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) y [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

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

 

