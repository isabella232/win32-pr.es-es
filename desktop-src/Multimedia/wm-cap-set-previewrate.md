---
title: Mensaje de WM_CAP_SET_PREVIEWRATE (VFW. h)
description: El \_ \_ mensaje PREVIEWRATE del conjunto de límites de WM \_ establece la velocidad de presentación del marco en el modo de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Mensaje de WM_CAP_SET_PREVIEWRATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997058"
---
# <a name="wm_cap_set_previewrate-message"></a>\_ \_ Mensaje PREVIEWRATE de conjunto de Cap de WM \_

El **mensaje \_ \_ \_ PREVIEWRATE del conjunto de límites de WM** establece la velocidad de presentación del marco en el modo de vista previa. Puede enviar este mensaje explícitamente o mediante la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*
</dt> <dd>

Velocidad, en milisegundos, a la que se capturan y muestran los nuevos fotogramas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

El modo de vista previa utiliza recursos de CPU importantes. Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco. Durante la captura de vídeo en streaming, la tarea de vista previa tiene una prioridad más baja que la escritura de tramas en el disco, y los marcos de vista previa solo se muestran si no hay otros búferes disponibles para escritura.

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

 

 





