---
title: Mensaje de WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: El \_ \_ \_ mensaje de videosource de Cap de WM Dlg muestra un cuadro de diálogo en el que el usuario puede controlar el origen de vídeo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- Mensaje de WM_CAP_DLG_VIDEOSOURCE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490114"
---
# <a name="wm_cap_dlg_videosource-message"></a>\_Mensaje de \_ videosource de límite de WM Dlg \_

El mensaje de **\_ \_ \_ videosource de Cap de WM Dlg** muestra un cuadro de diálogo en el que el usuario puede controlar el origen de vídeo. El cuadro de diálogo origen del vídeo puede contener controles que seleccionen orígenes de entrada; modificar el matiz, el contraste y el brillo de la imagen; y modifique la calidad del vídeo antes de digitalizar las imágenes en el búfer de fotogramas. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El cuadro de diálogo origen de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo origen de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoSource** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

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

 

 





