---
title: WM_CAP_GET_STATUS mensaje (Vfw.h)
description: El mensaje GET STATUS de WM \_ CAP recupera el estado de la ventana de \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071679"
---
# <a name="wm_cap_get_status-message"></a>Mensaje \_ DE ESTADO GET \_ DE WM CAP \_

El **mensaje GET STATUS \_ \_ \_ de WM CAP** recupera el estado de la ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capGetStatus.**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus)


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

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Puntero a una [**estructura CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

La [**estructura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contiene el estado actual de la ventana de captura. Dado que este estado es dinámico y cambia en respuesta a varios mensajes, la aplicación debe inicializar esta estructura después de enviar el mensaje [**\_ \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) de WM CAP (o mediante la macro [**capDlgVideoFormat)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) y siempre que necesite habilitar elementos de menú o determinar el estado real de la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





