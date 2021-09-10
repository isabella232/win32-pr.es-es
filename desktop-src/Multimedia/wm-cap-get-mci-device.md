---
title: WM_CAP_GET_MCI_DEVICE mensaje (Vfw.h)
description: El mensaje GET MCI DEVICE de WM CAP recupera el nombre de un dispositivo MCI previamente establecido con el mensaje \_ \_ WM CAP SET \_ \_ \_ \_ \_ MCI \_ DEVICE. Puede enviar este mensaje explícitamente o mediante la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371545"
---
# <a name="wm_cap_get_mci_device-message"></a>Mensaje \_ GET \_ \_ MCI DEVICE \_ de WM CAP

El **mensaje \_ GET \_ \_ MCI DEVICE \_ de WM CAP** recupera el nombre de un dispositivo MCI previamente establecido con el mensaje WM CAP SET [**\_ \_ \_ MCI \_ DEVICE.**](wm-cap-set-mci-device.md) Puede enviar este mensaje explícitamente o mediante la macro [**capGetMCIDeviceName.**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename)


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Longitud, en bytes, del búfer al que hace referencia **szName.**

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

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

 

 





