---
title: Mensaje de WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: El \_ mensaje del \_ controlador Cap de WM \_ obtener \_ Cap devuelve las capacidades de hardware del controlador de captura conectado actualmente a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- Mensaje de WM_CAP_DRIVER_GET_CAPS de Windows multimedia
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
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535344"
---
# <a name="wm_cap_driver_get_caps-message"></a>Mensaje de obtención Cap del \_ controlador Cap de WM \_ \_ \_

El mensaje del **\_ controlador Cap de WM \_ \_ obtener \_ Cap** devuelve las capacidades de hardware del controlador de captura conectado actualmente a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .


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

Puntero a la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) para que contenga las capacidades de hardware.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

Las capacidades devueltas en [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) son constantes para un controlador de captura determinado. Las aplicaciones necesitan recuperar esta información una vez cuando el controlador de captura se conecta por primera vez a una ventana de captura.

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

 

 





