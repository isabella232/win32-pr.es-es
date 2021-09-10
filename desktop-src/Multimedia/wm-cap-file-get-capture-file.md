---
title: WM_CAP_FILE_GET_CAPTURE_FILE mensaje (Vfw.h)
description: El mensaje WM \_ CAP FILE GET CAPTURE FILE devuelve el nombre del archivo de captura \_ \_ \_ \_ actual. Puede enviar este mensaje explícitamente o mediante la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371431"
---
# <a name="wm_cap_file_get_capture_file-message"></a>Mensaje \_ GET \_ CAPTURE \_ \_ \_ FILE de WM CAP FILE

El **mensaje WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE** devuelve el nombre del archivo de captura actual. Puede enviar este mensaje explícitamente o mediante la macro [**capFileGetCaptureFile.**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile)


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, del búfer definido por la aplicación al que hace referencia **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a un búfer definido por la aplicación que se usa para devolver el nombre del archivo de captura como una cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

El nombre de archivo de captura predeterminado es C: \\CAPTURE.AVI.

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

 

 





