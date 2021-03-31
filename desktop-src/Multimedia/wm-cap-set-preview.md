---
title: Mensaje de WM_CAP_SET_PREVIEW (VFW. h)
description: El \_ mensaje de vista previa del límite de Cap de WM \_ \_ habilita o deshabilita el modo de vista previa.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Mensaje de WM_CAP_SET_PREVIEW de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151097"
---
# <a name="wm_cap_set_preview-message"></a>\_Mensaje de \_ \_ vista previa de límite de Cap de WM

El mensaje de **\_ \_ \_ vista previa del límite de Cap de WM** habilita o deshabilita el modo de vista previa. En el modo de vista previa, los fotogramas se transfieren del hardware de captura a la memoria del sistema y, a continuación, se muestran en la ventana de captura mediante funciones GDI. Puede enviar este mensaje explícitamente o mediante la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*formato*
</dt> <dd>

Marca de vista previa. Especifique **true** para que este parámetro habilite el modo de vista previa o **false** para deshabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El modo de vista previa utiliza recursos de CPU importantes. Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco. El miembro **fLiveWindow** de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de vista previa está habilitado actualmente.

Al habilitar el modo de vista previa se deshabilita automáticamente el modo de superposición.

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

 

 





