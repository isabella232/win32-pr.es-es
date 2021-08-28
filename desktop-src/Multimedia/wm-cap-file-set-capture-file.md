---
title: WM_CAP_FILE_SET_CAPTURE_FILE mensaje (Vfw.h)
description: El mensaje WM \_ CAP FILE SET CAPTURE FILE \_ \_ \_ \_ nombra el archivo usado para la captura de vídeo. Puede enviar este mensaje explícitamente o mediante la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9435a7f0790c8ffe88f6b7ea6228bb2f442b23f5dcb15e2722e59b75c671588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687025"
---
# <a name="wm_cap_file_set_capture_file-message"></a>Mensaje \_ WM CAP FILE SET CAPTURE \_ \_ \_ \_ FILE

El **mensaje WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE** nombra el archivo usado para la captura de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetCaptureFile.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile)


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene el nombre del archivo de captura que se usará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el nombre de archivo es correcto o **FALSE** si el nombre de archivo no es válido, o si la secuencia o la captura de fotograma único están en curso.

## <a name="remarks"></a>Comentarios

Este mensaje almacena el nombre de archivo en una estructura interna. No crea, asigna ni abre el archivo especificado. El nombre de archivo de captura predeterminado es C: \\CAPTURE.AVI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





