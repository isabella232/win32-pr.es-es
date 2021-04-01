---
title: Mensaje de WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: El \_ mensaje del \_ archivo de captura del \_ conjunto \_ de archivos de Cap de WM \_ nombra el archivo que se utiliza para la captura de vídeo. Puede enviar este mensaje explícitamente o mediante la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Mensaje de WM_CAP_FILE_SET_CAPTURE_FILE de Windows multimedia
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
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995910"
---
# <a name="wm_cap_file_set_capture_file-message"></a>\_Mensaje de \_ \_ archivo de captura de conjunto de archivos Cap \_ de WM \_

El mensaje del archivo de captura del conjunto de archivos de Cap de WM nombra el archivo que se utiliza para la captura de vídeo. **\_ \_ \_ \_ \_** Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a la cadena terminada en null que contiene el nombre del archivo de captura que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si el nombre de archivo no es válido o si la captura de streaming o de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Este mensaje almacena el nombre de archivo en una estructura interna. No crea, asigna ni abre el archivo especificado. El nombre de archivo de captura predeterminado es C: \\CAPTURE.AVI.

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

 

 





