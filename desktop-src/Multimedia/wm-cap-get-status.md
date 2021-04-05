---
title: Mensaje de WM_CAP_GET_STATUS (VFW. h)
description: El \_ \_ \_ mensaje de estado de Cap de WM Get recupera el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Mensaje de WM_CAP_GET_STATUS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078834"
---
# <a name="wm_cap_get_status-message"></a>\_Mensaje de \_ Estado de obtención de Cap de WM \_

El mensaje de **Estado de Cap de WM \_ \_ \_ Get** recupera el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*seg*
</dt> <dd>

Puntero a una estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

La estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contiene el estado actual de la ventana de captura. Dado que este estado es dinámico y cambia en respuesta a varios mensajes, la aplicación debe inicializar esta estructura después de enviar el mensaje de [**\_ \_ \_ videoformat de Cap Cap de WM**](wm-cap-dlg-videoformat.md) (o mediante la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) y siempre que necesite habilitar elementos de menú o determinar el estado real de la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





