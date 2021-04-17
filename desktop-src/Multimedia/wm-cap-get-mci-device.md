---
title: Mensaje de WM_CAP_GET_MCI_DEVICE (VFW. h)
description: El \_ mensaje Cap \_ de WM Get \_ MCI \_ Device recupera el nombre de un dispositivo MCI previamente establecido con el \_ \_ mensaje de \_ dispositivo MCI del conjunto de Cap de WM \_ . Puede enviar este mensaje explícitamente o mediante la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- Mensaje de WM_CAP_GET_MCI_DEVICE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488963"
---
# <a name="wm_cap_get_mci_device-message"></a>\_Mensaje de \_ \_ dispositivo MCI de obtención de Cap de WM \_

El **mensaje \_ Cap de WM \_ Get \_ MCI \_ Device** recupera el nombre de un dispositivo MCI previamente establecido con el mensaje de [**\_ \_ \_ \_ dispositivo MCI del conjunto de Cap de WM**](wm-cap-set-mci-device.md) . Puede enviar este mensaje explícitamente o mediante la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Longitud, en bytes, del búfer al que se hace referencia en **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

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

 

 





