---
title: Mensaje de ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: El \_ \_ \_ mensaje de obtención de formato ICM descomprime solicita el formato de salida de los datos descomprimidos de un controlador de descompresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- Mensaje de ICM_DECOMPRESS_GET_FORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079644"
---
# <a name="icm_decompress_get_format-message"></a>Descompresión ICM \_ \_ Get \_ Format Message

El mensaje de **\_ obtención de \_ \_ formato ICM descomprime** solicita el formato de salida de los datos descomprimidos de un controlador de descompresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida. Puede especificar cero para solicitar solo el tamaño del formato de salida, como en la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si *lpbiOutput* es cero, devuelve el tamaño de la estructura.

Si *lpbiOutput* es distinto de cero, devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si *lpbiOutput* es distinto de cero, el controlador debe rellenar la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con el formato de salida predeterminado correspondiente al formato de entrada especificado para *lpbiInput*. Si el compresor puede generar varios formatos, el formato predeterminado debe ser el que conserva la mayor cantidad de información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

