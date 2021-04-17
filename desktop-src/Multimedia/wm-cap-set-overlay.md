---
title: Mensaje de WM_CAP_SET_OVERLAY (VFW. h)
description: El \_ mensaje de superposición de conjunto de Cap de WM \_ \_ habilita o deshabilita el modo de superposición. En el modo de superposición, el vídeo se muestra mediante la superposición de hardware. Puede enviar este mensaje explícitamente o mediante la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- Mensaje de WM_CAP_SET_OVERLAY de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676963"
---
# <a name="wm_cap_set_overlay-message"></a>\_Mensaje de \_ superposición de conjunto de Cap de WM \_

El mensaje de **\_ \_ \_ superposición de conjunto de Cap de WM** habilita o deshabilita el modo de superposición. En el modo de superposición, el vídeo se muestra mediante la superposición de hardware. Puede enviar este mensaje explícitamente o mediante la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*formato*
</dt> <dd>

Marca de superposición. Especifique **true** para este parámetro para habilitar el modo de superposición o **false** para deshabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El uso de una superposición no requiere recursos de CPU.

El miembro **fHasOverlay** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica si el dispositivo es capaz de superponerse. El miembro **fOverlayWindow** de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de superposición está habilitado actualmente.

Al habilitar el modo de superposición, se deshabilita automáticamente el modo vista previa.

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

 

 





