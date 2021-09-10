---
title: WM_CAP_FILE_SAVEAS mensaje (Vfw.h)
description: El mensaje \_ SAVEAS de WM CAP \_ FILE copia el contenido del archivo de captura en otro \_ archivo. Puede enviar este mensaje explícitamente o mediante la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371432"
---
# <a name="wm_cap_file_saveas-message"></a>Mensaje \_ \_ SAVEAS de ARCHIVO DE WM CAP \_

El **mensaje \_ \_ \_ SAVEAS de WM CAP FILE** copia el contenido del archivo de captura en otro archivo. Puede enviar este mensaje explícitamente o mediante la [**macro capFileSaveAs.**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas)


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a la cadena terminada en NULL que contiene el nombre del archivo de destino utilizado para copiar el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Este mensaje no cambia el nombre ni el contenido del archivo de captura actual.

Si la operación de copia no se realiza correctamente debido a un error de disco completo, el archivo de destino se elimina automáticamente.

Normalmente, se preasigna un archivo de captura para el segmento de captura más grande previsto y solo se puede usar una parte de él para capturar datos. Este mensaje copia solo la parte del archivo que contiene los datos de captura.

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

 

 





