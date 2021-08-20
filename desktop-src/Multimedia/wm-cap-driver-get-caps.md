---
title: WM_CAP_DRIVER_GET_CAPS mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ DRIVER GET \_ \_ CAPS devuelve las funcionalidades de hardware del controlador de captura conectado actualmente a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecc863234cddf64bece47896015fd01e97093d227951aef69363136e55cabe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687085"
---
# <a name="wm_cap_driver_get_caps-message"></a>Mensaje \_ GET \_ \_ CAPS DEL CONTROLADOR WM CAP \_

El **mensaje WM CAP DRIVER GET \_ \_ \_ \_ CAPS** devuelve las funcionalidades de hardware del controlador de captura conectado actualmente a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capDriverGetCaps.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*
</dt> <dd>

Puntero a la [**estructura CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) para contener las funcionalidades de hardware.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Comentarios

Las funcionalidades devueltas [**en CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) son constantes para un controlador de captura determinado. Las aplicaciones necesitan recuperar esta información una vez cuando el controlador de captura se conecta por primera vez a una ventana de captura.

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

 

 





