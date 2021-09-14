---
title: WM_CAP_SET_PREVIEW mensaje (Vfw.h)
description: El mensaje WM \_ CAP SET PREVIEW habilita o deshabilita el modo de vista \_ \_ previa.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161319"
---
# <a name="wm_cap_set_preview-message"></a>Mensaje WM \_ CAP \_ SET \_ PREVIEW

El **mensaje WM CAP SET \_ \_ \_ PREVIEW** habilita o deshabilita el modo de vista previa. En el modo de vista previa, los fotogramas se transfieren desde el hardware de captura a la memoria del sistema y, a continuación, se muestran en la ventana de captura mediante funciones GDI. Puede enviar este mensaje explícitamente o mediante la [**macro capPreview.**](/windows/desktop/api/Vfw/nf-vfw-cappreview)


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Marca de vista previa. Especifique **TRUE para** este parámetro para habilitar el modo de vista previa o **FALSE** para deshabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

El modo de versión preliminar usa recursos de CPU considerables. Las aplicaciones pueden deshabilitar la vista previa o reducir la velocidad de vista previa cuando otra aplicación tiene el foco. El **miembro fLiveWindow** de la [**estructura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica si el modo de vista previa está habilitado actualmente.

Al habilitar el modo de vista previa, se deshabilita automáticamente el modo de superposición.

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

 

 





