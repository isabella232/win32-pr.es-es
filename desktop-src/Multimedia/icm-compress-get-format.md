---
title: ICM_COMPRESS_GET_FORMAT mensaje (Vfw.h)
description: El ICM mensaje COMPRESS GET FORMAT solicita el formato de salida de los datos \_ \_ \_ comprimidos desde un controlador de compresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370424"
---
# <a name="icm_compress_get_format-message"></a>\_ICM Mensaje COMPRESS \_ GET \_ FORMAT

El **ICM mensaje COMPRESS GET \_ \_ \_ FORMAT** solicita el formato de salida de los datos comprimidos desde un controlador de compresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressGetFormat.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat)


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida. Puede especificar cero para este parámetro para solicitar solo el tamaño del formato de salida, como en la macro [**ICCompressGetFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si *lpbiOutput* es cero, devuelve el tamaño de la estructura.

Si *lpbiOutput* es distinto de cero, devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si *lpbiOutput* es distinto de cero, el controlador debe rellenar la estructura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con el formato de salida predeterminado correspondiente al formato de entrada especificado para *lpbiInput*. Si el producto puede generar varios formatos, el formato predeterminado debe ser el que conserve la mayor cantidad de información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

