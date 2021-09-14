---
title: WM_CAP_SET_OVERLAY mensaje (Vfw.h)
description: El mensaje \_ WM CAP SET OVERLAY habilita o deshabilita el modo de \_ \_ superposición. En el modo de superposición, el vídeo se muestra mediante la superposición de hardware. Puede enviar este mensaje explícitamente o mediante la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161321"
---
# <a name="wm_cap_set_overlay-message"></a>Mensaje \_ DE \_ SUPERPOSICIÓN \_ DE WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ OVERLAY** habilita o deshabilita el modo de superposición. En el modo de superposición, el vídeo se muestra mediante la superposición de hardware. Puede enviar este mensaje explícitamente o mediante la [**macro capOverlay.**](/windows/desktop/api/Vfw/nf-vfw-capoverlay)


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Marca de superposición. Especifique **TRUE** para este parámetro para habilitar el modo de **superposición** o FALSE para deshabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

El uso de una superposición no requiere recursos de CPU.

El **miembro fHasOverlay** de la [**estructura CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica si el dispositivo es capaz de superponer. El **miembro fOverlayWindow** de la [**estructura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de superposición está habilitado actualmente.

Al habilitar el modo de superposición, se deshabilita automáticamente el modo de vista previa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





