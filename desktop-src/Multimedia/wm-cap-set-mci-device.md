---
title: WM_CAP_SET_MCI_DEVICE mensaje (Vfw.h)
description: El mensaje WM CAP SET MCI DEVICE especifica el nombre del dispositivo de vídeo MCI que \_ se usará para capturar \_ \_ \_ datos. Puede enviar este mensaje explícitamente o mediante la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE mensaje Windows Multimedia
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
ms.openlocfilehash: f2df82b171e2353b51198fcd4a908abb586d981417c3fd14e5a81731975012aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622184"
---
# <a name="wm_cap_set_mci_device-message"></a>Mensaje \_ WM CAP SET \_ \_ MCI \_ DEVICE

El **mensaje WM CAP SET \_ \_ \_ MCI \_ DEVICE** especifica el nombre del dispositivo de vídeo MCI que se usará para capturar datos. Puede enviar este mensaje explícitamente o mediante la [**macro capSetMCIDeviceName.**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename)


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

Este mensaje almacena el nombre del dispositivo MCI en una estructura interna. No abre ni accede al dispositivo. El nombre predeterminado del dispositivo es **NULL.**

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

 

 





