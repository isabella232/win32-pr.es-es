---
title: Mensaje de WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: El \_ \_ \_ mensaje de Videopresentación de Cap de salida de WM muestra un cuadro de diálogo en el que el usuario puede establecer o ajustar la salida de vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- Mensaje de WM_CAP_DLG_VIDEODISPLAY de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996360"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>\_Mensaje de \_ vídeo de presentación de Cap \_ de WM

El mensaje de **\_ \_ \_ Videopresentación de Cap** de salida de WM muestra un cuadro de diálogo en el que el usuario puede establecer o ajustar la salida de vídeo. Este cuadro de diálogo puede contener controles que afectan al matiz, al contraste y al brillo de la imagen mostrada, así como a la alineación del color de la clave. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Los controles de este cuadro de diálogo no afectan a los datos de vídeo digitalizados; solo afectan a la salida o a la presentación de la señal de vídeo.

El cuadro de diálogo presentación en vídeo es único para cada controlador de captura. Es posible que algunos controladores de captura no admitan un cuadro de diálogo de presentación en vídeo. Las aplicaciones pueden determinar si el controlador de captura admite este mensaje comprobando el miembro **fHasDlgVideoDisplay** de la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

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

 

 





