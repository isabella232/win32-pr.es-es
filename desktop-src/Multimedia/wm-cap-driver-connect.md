---
title: WM_CAP_DRIVER_CONNECT mensaje (Vfw.h)
description: El mensaje WM \_ CAP DRIVER CONNECT conecta una ventana de captura a un controlador de \_ \_ captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473855"
---
# <a name="wm_cap_driver_connect-message"></a>Mensaje \_ WM CAP DRIVER \_ \_ CONNECT

El **mensaje WM CAP DRIVER \_ \_ \_ CONNECT** conecta una ventana de captura a un controlador de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capDriverConnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect)


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Índice del controlador de captura. El índice puede oscilar entre 0 y 9.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza **correctamente o FALSE** si el controlador de captura especificado no se puede conectar a la ventana de captura.

## <a name="remarks"></a>Observaciones

La conexión de un controlador de captura a una ventana de captura desconecta automáticamente cualquier controlador de captura conectado previamente.

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

 

 





