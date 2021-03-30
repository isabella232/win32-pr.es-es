---
title: Mensaje de WM_CAP_SET_MCI_DEVICE (VFW. h)
description: El \_ mensaje del \_ dispositivo MCI del conjunto de Cap de WM \_ \_ especifica el nombre del dispositivo de vídeo MCI que se va a usar para capturar los datos. Puede enviar este mensaje explícitamente o mediante la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Mensaje de WM_CAP_SET_MCI_DEVICE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801190"
---
# <a name="wm_cap_set_mci_device-message"></a>\_Mensaje de \_ \_ dispositivo MCI de conjunto de Cap de WM \_

El mensaje del **\_ \_ \_ \_ dispositivo MCI del conjunto de Cap de WM** especifica el nombre del dispositivo de vídeo MCI que se va a usar para capturar los datos. Puede enviar este mensaje explícitamente o mediante la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje almacena el nombre del dispositivo MCI en una estructura interna. No abre ni accede al dispositivo. El nombre de dispositivo predeterminado es **null**.

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

 

 





