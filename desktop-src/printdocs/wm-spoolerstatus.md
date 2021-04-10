---
description: El \_ mensaje de SPOOLERSTATUS de WM se envía desde el administrador de impresión siempre que se agrega o se quita un trabajo de la cola del administrador de impresión.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Mensaje de WM_SPOOLERSTATUS (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156648"
---
# <a name="wm_spoolerstatus-message"></a>Mensaje de SPOOLERSTATUS de WM \_

El mensaje de **\_ SPOOLERSTATUS de WM** se envía desde el administrador de impresión siempre que se agrega o se quita un trabajo de la cola del administrador de impresión.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

\_Marca JOBSTATUS de PR.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica el número de trabajos que quedan en la cola del administrador de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje es meramente informativo. Este mensaje es un aviso y no tiene una semántica de entrega garantizada. Las aplicaciones no deben suponer que recibirán un \_ mensaje de SPOOLERSTATUS de WM por cada cambio en el estado de la cola de impresión.

El mensaje de SPOOLERSTATUS de WM \_ no se admite después de Windows XP. Para recibir notificaciones de los cambios en el estado de la cola de impresión, puede usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) y [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Mensajes de la API del administrador de trabajos de impresión](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

