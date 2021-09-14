---
title: ICM_DECOMPRESS_GET_FORMAT mensaje (Vfw.h)
description: El ICM mensaje GET FORMAT de DECOMPRESS solicita el formato de salida de los datos \_ \_ \_ descomprimidos de un controlador de descompresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074230"
---
# <a name="icm_decompress_get_format-message"></a>\_ICM MENSAJE GET FORMAT DE DECOMPRESS \_ \_

El ICM mensaje GET FORMAT de **\_ DECOMPRESS \_ \_** solicita el formato de salida de los datos descomprimidos de un controlador de descompresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressGetFormat.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat)


```C++
ICM_DECOMPRESS_GET_FORMAT 
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

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida. Puede especificar cero para solicitar solo el tamaño del formato de salida, como en la macro [**ICDecompressGetFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize)

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

