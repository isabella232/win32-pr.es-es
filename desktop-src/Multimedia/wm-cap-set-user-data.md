---
title: Mensaje de WM_CAP_SET_USER_DATA (VFW. h)
description: El mensaje de datos del usuario del conjunto de límites de WM \_ \_ \_ \_ asocia un valor largo de \_ datos PTR a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- Mensaje de WM_CAP_SET_USER_DATA de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151095"
---
# <a name="wm_cap_set_user_data-message"></a>\_Mensaje de \_ datos de usuario del conjunto de Cap de \_ WM \_

El mensaje de **datos del usuario del conjunto de límites de WM \_ \_ \_ \_** asocia un valor largo de datos **\_ ptr** a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valor de datos que se va a asociar a una ventana de captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming está en curso.

## <a name="remarks"></a>Observaciones

Normalmente, este mensaje se usa para señalar a un bloque de datos asociado a una ventana de captura.

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

 

 





