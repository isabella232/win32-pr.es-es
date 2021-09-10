---
title: WM_CAP_SET_USER_DATA mensaje (Vfw.h)
description: El mensaje \_ WM CAP SET USER DATA asocia un valor de datos LONG \_ \_ \_ \_ PTR a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371450"
---
# <a name="wm_cap_set_user_data-message"></a>Mensaje DE DATOS DE USUARIO DE WM \_ CAP \_ SET \_ \_

El **mensaje WM CAP SET USER \_ \_ \_ \_ DATA** asocia un **valor de datos LONG \_ PTR** a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la [**macro capSetUserData.**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata)


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valor de datos que se asociará a una ventana de captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE** si la captura de streaming está en curso.

## <a name="remarks"></a>Observaciones

Normalmente, este mensaje se usa para apuntar a un bloque de datos asociado a una ventana de captura.

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

 

 





