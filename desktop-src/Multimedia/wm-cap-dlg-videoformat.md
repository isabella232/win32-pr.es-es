---
title: Mensaje de WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: El \_ mensaje de \_ vídeo de formato de Cap de WM Dlg \_ muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- Mensaje de WM_CAP_DLG_VIDEOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996267"
---
# <a name="wm_cap_dlg_videoformat-message"></a>\_Mensaje de \_ \_ videoformateador de Cap de WM

El mensaje de vídeo de **formato de Cap de WM \_ \_ \_ Dlg** muestra un cuadro de diálogo en el que el usuario puede seleccionar el formato de vídeo. El cuadro de diálogo formato de vídeo se puede usar para seleccionar las opciones dimensiones de imagen, profundidad de bits y compresión de hardware. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Una vez que se devuelve este mensaje, es posible que las aplicaciones necesiten actualizar la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque el usuario podría haber cambiado las dimensiones de la imagen.

El cuadro de diálogo formato de vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo formato de vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

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

 

 





