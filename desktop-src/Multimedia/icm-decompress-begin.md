---
title: ICM_DECOMPRESS_BEGIN mensaje (Vfw.h)
description: El ICM DECOMPRESS BEGIN notifica a un controlador \_ \_ de descompresión de vídeo que se prepare para descomprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678355"
---
# <a name="icm_decompress_begin-message"></a>\_ICM Mensaje BEGIN de \_ DECOMPRESS

El **ICM \_ DECOMPRESS \_ BEGIN** notifica a un controlador de descompresión de vídeo que se prepare para descomprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin)


```C++
ICM_DECOMPRESS_BEGIN 
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

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando el controlador recibe este mensaje, debe asignar búferes y realizar las operaciones que requieren mucho tiempo para que pueda procesar ICM [**\_ mensajes DECOMPRESS**](icm-decompress.md) de forma eficaz.

Si desea que el controlador descomprima los datos directamente en la pantalla, envíe el [**ICM \_ DRAW.**](icm-draw.md)

Los **ICM \_ DECOMPRESS \_ BEGIN** [**y ICM \_ end de DECOMPRESS \_ no**](icm-decompress-end.md) anidan. Si el controlador recibe **ICM \_ DECOMPRESS \_ BEGIN** antes de detener la descompresión con **ICM END de \_ DECOMPRESS, \_** debe reiniciar la descompresión con nuevos parámetros.

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

 

