---
title: WM_CAP_FILE_SAVEDIB mensaje (Vfw.h)
description: El mensaje SAVEDIB DEL ARCHIVO DE CAP DE WM \_ copia el marco actual en un archivo \_ \_ DIB. Puede enviar este mensaje explícitamente o mediante la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803815"
---
# <a name="wm_cap_file_savedib-message"></a>Mensaje \_ SAVEDIB DE ARCHIVO DE CAP \_ DE WM \_

El **mensaje \_ \_ \_ SAVEDIB DEL ARCHIVO DE CAP** DE WM copia el marco actual en un archivo DIB. Puede enviar este mensaje explícitamente o mediante la [**macro capFileSaveDIB.**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib)


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene el nombre del archivo DIB de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**DE ERROR WM CAP SET \_ \_ \_ CALLBACK, \_**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Comentarios

Si el controlador de captura proporciona fotogramas en un formato comprimido, esta llamada intenta descomprimir el marco antes de escribir el archivo.

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

 

 





