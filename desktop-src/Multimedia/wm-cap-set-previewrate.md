---
title: WM_CAP_SET_PREVIEWRATE mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ SET \_ PREVIEWRATE establece la velocidad de visualización de fotogramas en modo de vista previa. Puede enviar este mensaje explícitamente o mediante la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161320"
---
# <a name="wm_cap_set_previewrate-message"></a>Mensaje \_ WM CAP SET \_ \_ PREVIEWRATE

El **mensaje WM CAP SET \_ \_ \_ PREVIEWRATE** establece la velocidad de visualización de fotogramas en modo de vista previa. Puede enviar este mensaje explícitamente o mediante la [**macro capPreviewRate.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate)


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*
</dt> <dd>

Velocidad, en milisegundos, a la que se capturan y muestran nuevos fotogramas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza **correctamente o FALSE** si la ventana de captura no está conectada a un controlador de captura.

## <a name="remarks"></a>Observaciones

El modo de versión preliminar usa recursos de CPU considerables. Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco. Durante la captura de vídeo de streaming, la tarea de vista previa tiene menos prioridad que escribir fotogramas en el disco y los fotogramas de vista previa solo se muestran si no hay ningún otro búfer disponible para escritura.

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

 

 





