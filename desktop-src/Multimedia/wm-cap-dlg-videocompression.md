---
title: Mensaje de WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: El \_ \_ \_ mensaje de compresión de videocompresión de Cap de WM muestra un cuadro de diálogo en el que el usuario puede seleccionar un compresor para usarlo durante el proceso de captura.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Mensaje de WM_CAP_DLG_VIDEOCOMPRESSION de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079341"
---
# <a name="wm_cap_dlg_videocompression-message"></a>\_Mensaje de \_ compresión de \_ videocompresión de Cap de WM

El mensaje de **\_ compresión de \_ \_ videocompresión de Cap de WM** muestra un cuadro de diálogo en el que el usuario puede seleccionar un compresor para usarlo durante el proceso de captura. La lista de compresores disponibles puede variar con el formato de vídeo seleccionado en el cuadro de diálogo formato de vídeo del controlador de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Use este mensaje con controladores de captura que proporcionen fotogramas solo en \_ formato RGB de BI. Este mensaje es muy útil en la operación de captura por pasos para combinar la captura y la compresión en una sola operación. Es muy probable que la compresión de fotogramas con un compresor de software como parte de una operación de captura en tiempo real sea demasiado lenta.

La compresión no afecta a los fotogramas copiados en el portapapeles.

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

 

 





